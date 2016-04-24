<form method="" action="">
    {% csrf_token %}
    {{ form.as_p }}
    <input type="submit" value="" class="btn"/>
</form>