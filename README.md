# reg-input
запрет ввода, цифр, букв, мульти

<pre>
// Только русс буквы
$("[name=langrus]").bind("change keyup input click", function() {
	if (this.value.match(/[^а-яА-Я\s]/g)) {
		this.value = this.value.replace(/[^а-яА-Я\s]/g, "");
	}
});

// Только англ и русс буквы
$("[name=langmulti]").bind("change keyup input click", function() {
	if (this.value.match(/[^а-яА-Яa-zA-Z\s]/g)) {
		this.value = this.value.replace(/[^а-яА-Яa-zA-Z\s]/g, "");
	}
});

// Только цыфры
$("[name=number]").bind("change keyup input click", function() {
	if (this.value.match(/[^0-9]/g)) {
		this.value = this.value.replace(/[^0-9]/g, "");
	}
});
</pre>
