<script>
export default {
    name: "EventCard",
    props: ["item"]
}
</script>

<template>
    <div class="col-md-4 gy-4">
        <div class="card h-100">
            <h6 class="card-header">Data evento: {{ item.date }}</h6>
            <div class="card-body">
                <h5 class="card-title">{{ item.name }}</h5>
                <p class="card-text">Biglietti disponibili: {{ item.available_tickets }}</p>
                <router-link :to="{ name: 'Event-detail', params: { id: item.id } }" class="btn btn-primary">
                    <span>Apri dettagli evento</span>
                </router-link>
                <a href="#" class="btn btn-warning ms-2">Compra biglietti</a>
            </div>
        </div>
    </div>
</template>