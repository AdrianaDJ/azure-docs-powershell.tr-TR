---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 9d63c208daffe6e06da759ff929de120cab58c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751409"
---
# <span data-ttu-id="fde90-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="fde90-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="fde90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde90-102">SYNOPSIS</span></span>
<span data-ttu-id="fde90-103">Kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="fde90-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="fde90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fde90-104">SYNTAX</span></span>

### <span data-ttu-id="fde90-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fde90-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde90-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fde90-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde90-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fde90-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde90-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fde90-108">DESCRIPTION</span></span>
<span data-ttu-id="fde90-109">Kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="fde90-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="fde90-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fde90-110">EXAMPLES</span></span>

### <span data-ttu-id="fde90-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fde90-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="fde90-112">Tanımlayıcı verilen kayıt tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fde90-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="fde90-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fde90-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="fde90-114">Tam nitelikli kaynak kimliği verilen kayıt tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fde90-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="fde90-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="fde90-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="fde90-116">Nesneye verilen kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="fde90-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="fde90-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fde90-117">PARAMETERS</span></span>

### <span data-ttu-id="fde90-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="fde90-118">-AsJob</span></span>
<span data-ttu-id="fde90-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fde90-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fde90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde90-120">-DefaultProfile</span></span>
<span data-ttu-id="fde90-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fde90-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde90-122">-ID</span><span class="sxs-lookup"><span data-stu-id="fde90-122">-Id</span></span>
<span data-ttu-id="fde90-123">Kayıt tanımı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fde90-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="fde90-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fde90-124">-InputObject</span></span>
<span data-ttu-id="fde90-125">Kayıt tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fde90-125">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fde90-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fde90-126">-ResourceId</span></span>
<span data-ttu-id="fde90-127">Kayıt tanımının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fde90-127">ResourceId of the registration definition</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fde90-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="fde90-128">-Confirm</span></span>
<span data-ttu-id="fde90-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fde90-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde90-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde90-130">-WhatIf</span></span>
<span data-ttu-id="fde90-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fde90-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde90-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fde90-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde90-133">CommonParameters</span></span>
<span data-ttu-id="fde90-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fde90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde90-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fde90-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde90-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fde90-136">INPUTS</span></span>

### <span data-ttu-id="fde90-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fde90-137">None</span></span>

## <span data-ttu-id="fde90-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fde90-138">OUTPUTS</span></span>

### <span data-ttu-id="fde90-139">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="fde90-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="fde90-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fde90-140">NOTES</span></span>

## <span data-ttu-id="fde90-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fde90-141">RELATED LINKS</span></span>
