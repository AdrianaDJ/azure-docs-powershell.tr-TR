---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/new-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 9f4bea5ce1eaad0096ed36628704d9406047d5f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590996"
---
# <span data-ttu-id="bc193-101">New-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="bc193-101">New-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="bc193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc193-102">SYNOPSIS</span></span>
<span data-ttu-id="bc193-103">Yeni bir kullanıcı kimliği oluşturur veya mevcut bir kullanıcı tarafından atanan kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bc193-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc193-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc193-104">SYNTAX</span></span>

```
New-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc193-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc193-105">DESCRIPTION</span></span>
<span data-ttu-id="bc193-106">**Yeni-Azurermuseratandidentity** cmdlet 'i, yeni bir kullanıcı atanmış kimliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc193-106">The **New-AzureRmUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="bc193-107">Var olan bir kimlikle kullanıldığında, kimliği güncelledi.</span><span class="sxs-lookup"><span data-stu-id="bc193-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="bc193-108">Kimliğe Azure Kaynak Yöneticisi etiketleri eklemek için, lütfen Set-AzureRmResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc193-108">To add Azure Resource Manager tags to the identity, please use the Set-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="bc193-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc193-109">EXAMPLES</span></span>

### <span data-ttu-id="bc193-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc193-110">Example 1</span></span>
<span data-ttu-id="bc193-111">Bu örnek cmdlet, ResourceGroup **kaynak grubu altında** **ID1** adlı yeni bir kullanıcı atanmış kimliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc193-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="bc193-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bc193-112">Example 2</span></span>
<span data-ttu-id="bc193-113">Bu örnek cmdlet, westus bölgesindeki **Psrg** kaynak grubunun altında adı **ID1** olan yeni bir kullanıcı tarafından atanan kimlik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc193-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

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

## <span data-ttu-id="bc193-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc193-114">PARAMETERS</span></span>

### <span data-ttu-id="bc193-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="bc193-115">-AsJob</span></span>
<span data-ttu-id="bc193-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bc193-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc193-117">-DefaultProfile</span></span>
<span data-ttu-id="bc193-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc193-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="bc193-119">-Location</span></span>
<span data-ttu-id="bc193-120">Kimliğin oluşturulması gereken Azure bölgesi adı.</span><span class="sxs-lookup"><span data-stu-id="bc193-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc193-121">-Name</span></span>
<span data-ttu-id="bc193-122">Kimlik adı.</span><span class="sxs-lookup"><span data-stu-id="bc193-122">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc193-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc193-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bc193-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bc193-125">-Tag</span></span>
<span data-ttu-id="bc193-126">Kimlikle ilişkili Azure Resource Manager etiketleri.</span><span class="sxs-lookup"><span data-stu-id="bc193-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc193-127">-Confirm</span></span>
<span data-ttu-id="bc193-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc193-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc193-129">-WhatIf</span></span>
<span data-ttu-id="bc193-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc193-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc193-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc193-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc193-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc193-132">CommonParameters</span></span>
<span data-ttu-id="bc193-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc193-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc193-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc193-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc193-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc193-135">INPUTS</span></span>

### <span data-ttu-id="bc193-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc193-136">None</span></span>

## <span data-ttu-id="bc193-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc193-137">OUTPUTS</span></span>

### <span data-ttu-id="bc193-138">Microsoft. Azure. Commands. Managedserviceıdentity. modeller. Psuseratandidentity</span><span class="sxs-lookup"><span data-stu-id="bc193-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="bc193-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc193-139">NOTES</span></span>

## <span data-ttu-id="bc193-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc193-140">RELATED LINKS</span></span>