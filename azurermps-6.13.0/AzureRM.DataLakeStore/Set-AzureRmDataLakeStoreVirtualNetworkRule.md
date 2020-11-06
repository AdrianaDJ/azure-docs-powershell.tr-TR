---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589567"
---
# <span data-ttu-id="5cbe0-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5cbe0-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="5cbe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbe0-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbe0-103">Belirtilen veri Lake Store 'da belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cbe0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbe0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cbe0-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbe0-106">**Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet 'ı belirtilen veri Lake Store 'da belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-106">The **Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5cbe0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cbe0-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbe0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5cbe0-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="5cbe0-109">"DLS" hesabındaki "myVNET" sanal ağ kuralının alt ağ kimliğini "Güncelleştirmegerçekleşti" olarak güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="5cbe0-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="5cbe0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cbe0-110">PARAMETERS</span></span>

### <span data-ttu-id="5cbe0-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5cbe0-111">-Account</span></span>
<span data-ttu-id="5cbe0-112">Sanal ağ kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5cbe0-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="5cbe0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbe0-113">-DefaultProfile</span></span>
<span data-ttu-id="5cbe0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cbe0-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cbe0-115">-Name</span></span>
<span data-ttu-id="5cbe0-116">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="5cbe0-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5cbe0-117">-SubnetId</span></span>
<span data-ttu-id="5cbe0-118">Sanal ağ kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="5cbe0-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="5cbe0-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cbe0-119">-Confirm</span></span>
<span data-ttu-id="5cbe0-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbe0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbe0-121">-WhatIf</span></span>
<span data-ttu-id="5cbe0-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbe0-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbe0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbe0-124">CommonParameters</span></span>
<span data-ttu-id="5cbe0-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbe0-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbe0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbe0-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-127">INPUTS</span></span>

### <span data-ttu-id="5cbe0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5cbe0-128">System.String</span></span>

## <span data-ttu-id="5cbe0-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cbe0-129">OUTPUTS</span></span>

### <span data-ttu-id="5cbe0-130">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5cbe0-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="5cbe0-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cbe0-131">NOTES</span></span>

## <span data-ttu-id="5cbe0-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cbe0-132">RELATED LINKS</span></span>
