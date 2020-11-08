---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277335"
---
# <span data-ttu-id="05515-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="05515-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="05515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05515-102">SYNOPSIS</span></span>
<span data-ttu-id="05515-103">Kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="05515-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="05515-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05515-104">SYNTAX</span></span>

### <span data-ttu-id="05515-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05515-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05515-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="05515-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05515-107">Byauthorter</span><span class="sxs-lookup"><span data-stu-id="05515-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05515-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="05515-108">DESCRIPTION</span></span>
<span data-ttu-id="05515-109">Kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="05515-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="05515-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05515-110">EXAMPLES</span></span>

### <span data-ttu-id="05515-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05515-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="05515-112">Roledefinitionıd ve PrincipalId değerleri doğrudan verilen bir kayıt tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05515-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="05515-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="05515-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="05515-114">Yetkilendirme ayrıntılarını içeren bir kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="05515-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="05515-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="05515-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="05515-116">Kayıt tanımını, yetkilendirme ayrıntılarını ve kayıt tanımının adını kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="05515-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="05515-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05515-117">PARAMETERS</span></span>

### <span data-ttu-id="05515-118">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="05515-118">-Authorization</span></span>
<span data-ttu-id="05515-119">PrincipalId-Roledefinitionıd ile yetkilendirme eşleme listesi.</span><span class="sxs-lookup"><span data-stu-id="05515-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05515-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05515-120">-DefaultProfile</span></span>
<span data-ttu-id="05515-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05515-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05515-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="05515-122">-Description</span></span>
<span data-ttu-id="05515-123">Kayıt tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="05515-123">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="05515-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="05515-124">-DisplayName</span></span>
<span data-ttu-id="05515-125">Kayıt tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="05515-125">The display name of the Registration Definition.</span></span>

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

### <span data-ttu-id="05515-126">-Managedbytenantıd</span><span class="sxs-lookup"><span data-stu-id="05515-126">-ManagedByTenantId</span></span>
<span data-ttu-id="05515-127">ManagedBy kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="05515-127">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="05515-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="05515-128">-Name</span></span>
<span data-ttu-id="05515-129">Kayıt tanımının benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="05515-129">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="05515-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="05515-130">-PlanName</span></span>
<span data-ttu-id="05515-131">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="05515-131">The name of the plan.</span></span>

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

### <span data-ttu-id="05515-132">-Planürün</span><span class="sxs-lookup"><span data-stu-id="05515-132">-PlanProduct</span></span>
<span data-ttu-id="05515-133">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="05515-133">The name of the Product.</span></span>

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

### <span data-ttu-id="05515-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="05515-134">-PlanPublisher</span></span>
<span data-ttu-id="05515-135">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="05515-135">The name of the Publisher.</span></span>

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

### <span data-ttu-id="05515-136">-Plansürümü</span><span class="sxs-lookup"><span data-stu-id="05515-136">-PlanVersion</span></span>
<span data-ttu-id="05515-137">Planın sürüm numarası.</span><span class="sxs-lookup"><span data-stu-id="05515-137">The version number of the plan.</span></span>

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

### <span data-ttu-id="05515-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="05515-138">-PrincipalId</span></span>
<span data-ttu-id="05515-139">ManagedBy Principal tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="05515-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05515-140">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="05515-140">-RoleDefinitionId</span></span>
<span data-ttu-id="05515-141">Temel tanımlayıcıya izin vermek için rol tanımı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="05515-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05515-142">-Iş</span><span class="sxs-lookup"><span data-stu-id="05515-142">-AsJob</span></span>
<span data-ttu-id="05515-143">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="05515-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05515-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="05515-144">-Confirm</span></span>
<span data-ttu-id="05515-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05515-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05515-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05515-146">-WhatIf</span></span>
<span data-ttu-id="05515-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05515-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05515-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05515-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05515-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05515-149">CommonParameters</span></span>
<span data-ttu-id="05515-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05515-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05515-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="05515-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05515-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05515-152">INPUTS</span></span>

### <span data-ttu-id="05515-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="05515-153">None</span></span>
## <span data-ttu-id="05515-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05515-154">OUTPUTS</span></span>

### <span data-ttu-id="05515-155">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="05515-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="05515-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05515-156">NOTES</span></span>

## <span data-ttu-id="05515-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05515-157">RELATED LINKS</span></span>
