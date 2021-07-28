<template>
    <div>
        <div class="text-white mb-4">
            {{ barHeader.startDayNo }}
            {{ barHeader.startMonth }}
            {{ barHeader.startYear }} - {{ barHeader.endDay }}
            {{ barHeader.endDayNo }} {{ barHeader.endMonth }}
            {{ barHeader.endYear }}
        </div>
    </div>
</template>
<script>
export default {
	data() {
		return {
			barHeader: {
                startDayNo: String(lastWeek.getDate()).padStart(2, "0"),
                endDayNo: String(yesterday.getDate()).padStart(2, "0"),

                startMonthNo: String(lastWeek.getMonth()).padStart(2, "0"),
                endMonthNo: String(yesterday.getMonth()).padStart(2, "0"),
                startMonth: monthOfYear[lastWeek.getMonth()],
                endMonth: monthOfYear[yesterday.getMonth()],

                startYear: lastWeek.getFullYear(),
                endYear: yesterday.getFullYear()
            }
		}
	}
};

const today = new Date();
const yesterday = new Date(
    today.getFullYear(),
    today.getMonth(),
    today.getDate() - 1
);
const lastWeek = new Date(
    today.getFullYear(),
    today.getMonth(),
    today.getDate() - 7
);
const monthOfYear = [
    "JAN",
    "FEB",
    "MAR",
    "APR",
    "MAY",
    "JUN",
    "JUL",
    "AUG",
    "SEP",
    "OCT",
    "NOV",
    "DEC"
];

</script>
<style></style>
