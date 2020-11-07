---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 079ff61475405407fc2f6864d9fda43b1a5fc4cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752318"
---
# <span data-ttu-id="81f82-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="81f82-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="81f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f82-102">SYNOPSIS</span></span>
<span data-ttu-id="81f82-103">Belirtilen veri Lake Store 'da belirtilen sanal ağ kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="81f82-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="81f82-104">Sanal ağ kuralı belirtilmezse, hesabın tüm sanal ağ kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="81f82-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="81f82-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81f82-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81f82-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="81f82-106">DESCRIPTION</span></span>
<span data-ttu-id="81f82-107">Get-AzDataLakeStoreVirtualNetworkRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen sanal ağ kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="81f82-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="81f82-108">Sanal ağ kuralı belirtilmezse, hesabın tüm sanal ağ kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="81f82-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="81f82-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81f82-109">EXAMPLES</span></span>

### <span data-ttu-id="81f82-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="81f82-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="81f82-111">"MyVNET" adlı "DLS" hesabından sanal ağ kuralını döndürür</span><span class="sxs-lookup"><span data-stu-id="81f82-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="81f82-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81f82-112">PARAMETERS</span></span>

### <span data-ttu-id="81f82-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="81f82-113">-Account</span></span>
<span data-ttu-id="81f82-114">Sanal ağ kuralını alma</span><span class="sxs-lookup"><span data-stu-id="81f82-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="81f82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f82-115">-DefaultProfile</span></span>
<span data-ttu-id="81f82-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81f82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f82-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="81f82-117">-Name</span></span>
<span data-ttu-id="81f82-118">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="81f82-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="81f82-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f82-119">CommonParameters</span></span>
<span data-ttu-id="81f82-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81f82-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f82-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f82-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f82-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81f82-122">INPUTS</span></span>

### <span data-ttu-id="81f82-123">System. String</span><span class="sxs-lookup"><span data-stu-id="81f82-123">System.String</span></span>

## <span data-ttu-id="81f82-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81f82-124">OUTPUTS</span></span>

### <span data-ttu-id="81f82-125">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="81f82-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="81f82-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81f82-126">NOTES</span></span>

## <span data-ttu-id="81f82-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81f82-127">RELATED LINKS</span></span>