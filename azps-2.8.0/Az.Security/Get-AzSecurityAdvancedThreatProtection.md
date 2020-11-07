---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 13ab536d08de0092523f860defe04a6e973d90e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932510"
---
# <span data-ttu-id="db79a-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="db79a-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="db79a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db79a-102">SYNOPSIS</span></span>
<span data-ttu-id="db79a-103">Storage/cosmosDB hesabı için Gelişmiş tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="db79a-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="db79a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db79a-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db79a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db79a-105">DESCRIPTION</span></span>
<span data-ttu-id="db79a-106">`Get-AzSecurityAdvancedThreatProtection`Cmdlet, bir depolama/cosmosDB hesabı için tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="db79a-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="db79a-107">Bu cmdlet 'i kullanmak için *RESOURCEID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="db79a-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="db79a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db79a-108">EXAMPLES</span></span>

### <span data-ttu-id="db79a-109">Örnek 1: depolama hesabı</span><span class="sxs-lookup"><span data-stu-id="db79a-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="db79a-110">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini alır `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="db79a-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="db79a-111">Örnek 2: CosmosDB hesabı</span><span class="sxs-lookup"><span data-stu-id="db79a-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="db79a-112">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini alır ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="db79a-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="db79a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db79a-113">PARAMETERS</span></span>

### <span data-ttu-id="db79a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db79a-114">-DefaultProfile</span></span>
<span data-ttu-id="db79a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db79a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db79a-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="db79a-116">-ResourceId</span></span>
<span data-ttu-id="db79a-117">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="db79a-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="db79a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db79a-118">CommonParameters</span></span>
<span data-ttu-id="db79a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db79a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db79a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db79a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db79a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db79a-121">INPUTS</span></span>

### <span data-ttu-id="db79a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="db79a-122">System.String</span></span>

## <span data-ttu-id="db79a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db79a-123">OUTPUTS</span></span>

### <span data-ttu-id="db79a-124">Microsoft. Azure. Commands. Security. modeller. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="db79a-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="db79a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db79a-125">NOTES</span></span>

## <span data-ttu-id="db79a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db79a-126">RELATED LINKS</span></span>
