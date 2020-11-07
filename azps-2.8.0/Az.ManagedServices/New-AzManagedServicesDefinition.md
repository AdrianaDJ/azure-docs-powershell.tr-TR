---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 8bcf260156584ddf7c8c2ac0ec347a59214f20c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751413"
---
# <span data-ttu-id="84032-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="84032-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="84032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84032-102">SYNOPSIS</span></span>
<span data-ttu-id="84032-103">Kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84032-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="84032-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84032-104">SYNTAX</span></span>

### <span data-ttu-id="84032-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84032-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84032-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="84032-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84032-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84032-107">DESCRIPTION</span></span>
<span data-ttu-id="84032-108">Kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84032-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="84032-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84032-109">EXAMPLES</span></span>

### <span data-ttu-id="84032-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84032-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="84032-111">Gerekli parametreler verildiğinde bir kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84032-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="84032-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="84032-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="84032-113">Plan detaylarla bir kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84032-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="84032-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84032-114">PARAMETERS</span></span>

### <span data-ttu-id="84032-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="84032-115">-AsJob</span></span>
<span data-ttu-id="84032-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="84032-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84032-117">-DefaultProfile</span></span>
<span data-ttu-id="84032-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84032-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="84032-119">-Description</span></span>
<span data-ttu-id="84032-120">Kayıt tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="84032-120">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-121">-Managedbytenantıd</span><span class="sxs-lookup"><span data-stu-id="84032-121">-ManagedByTenantId</span></span>
<span data-ttu-id="84032-122">ManagedBy kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="84032-122">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="84032-123">-PlanName</span></span>
<span data-ttu-id="84032-124">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="84032-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-125">-Planürün</span><span class="sxs-lookup"><span data-stu-id="84032-125">-PlanProduct</span></span>
<span data-ttu-id="84032-126">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="84032-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="84032-127">-PlanPublisher</span></span>
<span data-ttu-id="84032-128">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="84032-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-129">-Plansürümü</span><span class="sxs-lookup"><span data-stu-id="84032-129">-PlanVersion</span></span>
<span data-ttu-id="84032-130">Planın sürüm numarası.</span><span class="sxs-lookup"><span data-stu-id="84032-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="84032-131">-PrincipalId</span></span>
<span data-ttu-id="84032-132">ManagedBy Principal tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="84032-132">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="84032-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="84032-134">Kayıt tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="84032-134">The name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-135">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="84032-135">-RoleDefinitionId</span></span>
<span data-ttu-id="84032-136">Yönetilen hizmet sağlayıcısının rol tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="84032-136">The Managed Service Provider's Role Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="84032-137">-Confirm</span></span>
<span data-ttu-id="84032-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84032-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84032-139">-WhatIf</span></span>
<span data-ttu-id="84032-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84032-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84032-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84032-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84032-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84032-142">CommonParameters</span></span>
<span data-ttu-id="84032-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84032-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84032-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="84032-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84032-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84032-145">INPUTS</span></span>

### <span data-ttu-id="84032-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="84032-146">None</span></span>

## <span data-ttu-id="84032-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84032-147">OUTPUTS</span></span>

### <span data-ttu-id="84032-148">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="84032-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="84032-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84032-149">NOTES</span></span>

## <span data-ttu-id="84032-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84032-150">RELATED LINKS</span></span>
