---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: d4d2ae2ae8b09f319efe2f77030c88338b4c40b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104307"
---
# <span data-ttu-id="081b7-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="081b7-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="081b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="081b7-102">SYNOPSIS</span></span>
<span data-ttu-id="081b7-103">Storage/cosmosDB hesabı için Gelişmiş tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="081b7-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="081b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="081b7-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="081b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="081b7-105">DESCRIPTION</span></span>
<span data-ttu-id="081b7-106">`Get-AzSecurityAdvancedThreatProtection`Cmdlet, bir depolama/cosmosDB hesabı için tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="081b7-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="081b7-107">Bu cmdlet 'i kullanmak için *RESOURCEID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="081b7-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="081b7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="081b7-108">EXAMPLES</span></span>

### <span data-ttu-id="081b7-109">Örnek 1: depolama hesabı</span><span class="sxs-lookup"><span data-stu-id="081b7-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="081b7-110">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini alır `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="081b7-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="081b7-111">Örnek 2: CosmosDB hesabı</span><span class="sxs-lookup"><span data-stu-id="081b7-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="081b7-112">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini alır ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="081b7-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="081b7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="081b7-113">PARAMETERS</span></span>

### <span data-ttu-id="081b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081b7-114">-DefaultProfile</span></span>
<span data-ttu-id="081b7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="081b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="081b7-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="081b7-116">-ResourceId</span></span>
<span data-ttu-id="081b7-117">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="081b7-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081b7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081b7-118">CommonParameters</span></span>
<span data-ttu-id="081b7-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="081b7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081b7-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081b7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081b7-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="081b7-121">INPUTS</span></span>

### <span data-ttu-id="081b7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="081b7-122">System.String</span></span>

## <span data-ttu-id="081b7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="081b7-123">OUTPUTS</span></span>

### <span data-ttu-id="081b7-124">Microsoft. Azure. Commands. Security. modeller. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="081b7-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="081b7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="081b7-125">NOTES</span></span>

## <span data-ttu-id="081b7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="081b7-126">RELATED LINKS</span></span>
