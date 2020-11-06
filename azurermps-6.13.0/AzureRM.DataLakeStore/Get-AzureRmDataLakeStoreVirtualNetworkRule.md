---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588484"
---
# <span data-ttu-id="37365-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="37365-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="37365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37365-102">SYNOPSIS</span></span>
<span data-ttu-id="37365-103">Belirtilen veri Lake Store 'da belirtilen sanal ağ kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="37365-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="37365-104">Sanal ağ kuralı belirtilmezse, hesabın tüm sanal ağ kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="37365-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37365-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37365-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37365-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="37365-106">DESCRIPTION</span></span>
<span data-ttu-id="37365-107">Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen sanal ağ kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="37365-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="37365-108">Sanal ağ kuralı belirtilmezse, hesabın tüm sanal ağ kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="37365-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="37365-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37365-109">EXAMPLES</span></span>

### <span data-ttu-id="37365-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37365-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="37365-111">"MyVNET" adlı "DLS" hesabından sanal ağ kuralını döndürür</span><span class="sxs-lookup"><span data-stu-id="37365-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="37365-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37365-112">PARAMETERS</span></span>

### <span data-ttu-id="37365-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="37365-113">-Account</span></span>
<span data-ttu-id="37365-114">Sanal ağ kuralını alma</span><span class="sxs-lookup"><span data-stu-id="37365-114">The Data Lake Store account to get the virtual network rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37365-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37365-115">-DefaultProfile</span></span>
<span data-ttu-id="37365-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37365-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37365-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="37365-117">-Name</span></span>
<span data-ttu-id="37365-118">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="37365-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="37365-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37365-119">CommonParameters</span></span>
<span data-ttu-id="37365-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37365-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37365-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37365-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37365-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37365-122">INPUTS</span></span>

### <span data-ttu-id="37365-123">System. String</span><span class="sxs-lookup"><span data-stu-id="37365-123">System.String</span></span>

## <span data-ttu-id="37365-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37365-124">OUTPUTS</span></span>

### <span data-ttu-id="37365-125">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="37365-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="37365-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37365-126">NOTES</span></span>

## <span data-ttu-id="37365-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37365-127">RELATED LINKS</span></span>
