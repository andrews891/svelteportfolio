<head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.5.0/font/bootstrap-icons.css">
</head>

<script>
    import {
      Collapse,
      Navbar,
      NavbarToggler,
      NavbarBrand,
      Nav,
      NavItem,
      NavLink,
      Icon
    } from 'sveltestrap';

    let isOpen = false;

    function handleUpdate(event) {
        isOpen = event.detail.isOpen;
    }
</script>

<main>
    <Navbar color="dark" dark expand="md">
        <NavbarBrand href="/"></NavbarBrand>
        <NavbarToggler on:click={() => (isOpen = !isOpen)} />
        <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
            <Nav class="ms-auto" navbar>
                <NavItem>
                    <NavLink href="https://github.com/andrews891" target="_blank">
                        <Icon name="github"/>
                    </NavLink>
                </NavItem>
                <NavItem>
                    <NavLink href="https://twitter.com/andrewms404" target="_blank">
                        <Icon name="twitter"/>
                    </NavLink>
                </NavItem>
            </Nav>
        </Collapse>
    </Navbar>
</main>