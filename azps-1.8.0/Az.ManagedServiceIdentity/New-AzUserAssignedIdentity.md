---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 572e3d61f4d7cf514cc44fe965a7726288806a9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915823"
---
# <span data-ttu-id="3cd76-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3cd76-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="3cd76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd76-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd76-103">Yeni bir kullanıcı kimliği oluşturur veya mevcut bir kullanıcı tarafından atanan kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3cd76-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="3cd76-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cd76-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cd76-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cd76-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd76-106">**New-Azuseratanandentity** cmdlet 'i, yeni bir kullanıcı atanmış kimliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3cd76-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="3cd76-107">Var olan bir kimlikle kullanıldığında, kimliği güncelledi.</span><span class="sxs-lookup"><span data-stu-id="3cd76-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="3cd76-108">Kimliğe Azure Kaynak Yöneticisi etiketleri eklemek için, lütfen Set-AzResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3cd76-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="3cd76-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cd76-109">EXAMPLES</span></span>

### <span data-ttu-id="3cd76-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3cd76-110">Example 1</span></span>
<span data-ttu-id="3cd76-111">Bu örnek cmdlet, ResourceGroup **kaynak grubu altında** **ID1** adlı yeni bir kullanıcı atanmış kimliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3cd76-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="3cd76-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3cd76-112">Example 2</span></span>
<span data-ttu-id="3cd76-113">Bu örnek cmdlet, westus bölgesindeki **Psrg** kaynak grubunun altında adı **ID1** olan yeni bir kullanıcı tarafından atanan kimlik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3cd76-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="3cd76-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cd76-114">PARAMETERS</span></span>

### <span data-ttu-id="3cd76-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="3cd76-115">-AsJob</span></span>
<span data-ttu-id="3cd76-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3cd76-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cd76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd76-117">-DefaultProfile</span></span>
<span data-ttu-id="3cd76-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3cd76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd76-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="3cd76-119">-Location</span></span>
<span data-ttu-id="3cd76-120">Kimliğin oluşturulması gereken Azure bölgesi adı.</span><span class="sxs-lookup"><span data-stu-id="3cd76-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd76-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cd76-121">-Name</span></span>
<span data-ttu-id="3cd76-122">Kimlik adı.</span><span class="sxs-lookup"><span data-stu-id="3cd76-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd76-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd76-123">-ResourceGroupName</span></span>
<span data-ttu-id="3cd76-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3cd76-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd76-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3cd76-125">-Tag</span></span>
<span data-ttu-id="3cd76-126">Kimlikle ilişkili Azure Resource Manager etiketleri.</span><span class="sxs-lookup"><span data-stu-id="3cd76-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd76-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cd76-127">-Confirm</span></span>
<span data-ttu-id="3cd76-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cd76-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd76-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd76-129">-WhatIf</span></span>
<span data-ttu-id="3cd76-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cd76-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd76-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cd76-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd76-132">CommonParameters</span></span>
<span data-ttu-id="3cd76-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cd76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd76-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd76-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd76-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cd76-135">INPUTS</span></span>

### <span data-ttu-id="3cd76-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3cd76-136">System.String</span></span>

### <span data-ttu-id="3cd76-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cd76-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3cd76-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cd76-138">OUTPUTS</span></span>

### <span data-ttu-id="3cd76-139">Microsoft. Azure. Commands. Managedserviceıdentity. modeller. Psuseratandidentity</span><span class="sxs-lookup"><span data-stu-id="3cd76-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="3cd76-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cd76-140">NOTES</span></span>

## <span data-ttu-id="3cd76-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cd76-141">RELATED LINKS</span></span>