---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/get-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Get-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Get-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 0d7d3e035c65ce668eb8858500ed7fed17af37af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762602"
---
# <span data-ttu-id="8501d-101">Get-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8501d-101">Get-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="8501d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8501d-102">SYNOPSIS</span></span>
<span data-ttu-id="8501d-103">Kullanıcı tarafından atanan kimliği/kimlikleri alır.</span><span class="sxs-lookup"><span data-stu-id="8501d-103">Gets User Assigned Identity/identities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8501d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8501d-104">SYNTAX</span></span>

### <span data-ttu-id="8501d-105">SuscriptionParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8501d-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzureRmUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8501d-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8501d-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8501d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8501d-107">DESCRIPTION</span></span>
<span data-ttu-id="8501d-108">**Get-Azurermuseratandidentity** , mevcut kullanıcı tarafından atanmış kimlikleri alır.</span><span class="sxs-lookup"><span data-stu-id="8501d-108">The **Get-AzureRmUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="8501d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8501d-109">EXAMPLES</span></span>

### <span data-ttu-id="8501d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8501d-110">Example 1</span></span>
<span data-ttu-id="8501d-111">Bu örnek cmdlet, Kullanıcı tarafından atanan kimliği **ID1** **PSRG**</span><span class="sxs-lookup"><span data-stu-id="8501d-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="8501d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8501d-112">Example 2</span></span>
<span data-ttu-id="8501d-113">Bu örnek cmdlet, Kullanıcı tarafından atanan tüm kimlikleri **Psrg** kaynak grubu altında alır</span><span class="sxs-lookup"><span data-stu-id="8501d-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="8501d-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8501d-114">Example 3</span></span>
<span data-ttu-id="8501d-115">Bu örnek cmdlet, aboneliğin altındaki tüm Kullanıcı kimliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="8501d-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="8501d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8501d-116">PARAMETERS</span></span>

### <span data-ttu-id="8501d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8501d-117">-DefaultProfile</span></span>
<span data-ttu-id="8501d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8501d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8501d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8501d-119">-Name</span></span>
<span data-ttu-id="8501d-120">Kimlik adı.</span><span class="sxs-lookup"><span data-stu-id="8501d-120">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8501d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8501d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8501d-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8501d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8501d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8501d-123">CommonParameters</span></span>
<span data-ttu-id="8501d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8501d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8501d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8501d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8501d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8501d-126">INPUTS</span></span>

### <span data-ttu-id="8501d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8501d-127">System.String</span></span>

## <span data-ttu-id="8501d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8501d-128">OUTPUTS</span></span>

### <span data-ttu-id="8501d-129">Microsoft. Azure. Commands. Managedserviceıdentity. modeller. Psuseratandidentity</span><span class="sxs-lookup"><span data-stu-id="8501d-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="8501d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8501d-130">NOTES</span></span>

## <span data-ttu-id="8501d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8501d-131">RELATED LINKS</span></span>