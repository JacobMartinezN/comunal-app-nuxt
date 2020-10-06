<template>
    <div class="breadcrumb-section">
        <div class="content">
            <h1> Mis problemas</h1>
              <div class="page__section">
                <nav aria-label="breadcrumb">
                    <ol class="breadcrumb">
                        <li class="breadcrumb-item"><a href="#">Problemas</a></li>
                        <li class="breadcrumb-item active" aria-current="page">Mis problemas</li>
                    </ol>
                </nav>
            </div>
        </div>
    </div>
</template>

<style>
    .breadcrumb-section {
        overflow: hidden;
        background-color: #ffffff;
        padding: 20px 10px 0 10px;
        box-shadow: 0 26px 40px -24px rgba(128, 152, 213, 0.15);
        margin-bottom: 30px;
    }

    .breadcrumb {
        display: flex;
        flex-wrap: wrap;
        padding: .75rem 0;
        margin-bottom: 1rem;
        list-style: none
    }

    .breadcrumb-item {
        display: flex;
    }

    .breadcrumb-item a {
        text-decoration: none;
        color: #16afd1;
    }

    .breadcrumb-item+.breadcrumb-item {
        padding-left: .5rem;
    }

    .breadcrumb-item+.breadcrumb-item::before {
        display: inline-block;
        padding-right: .5rem;
        color: #6c757d;
        content: ">";
    }
</style>