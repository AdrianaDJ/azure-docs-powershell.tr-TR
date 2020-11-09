---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320625"
---
# <span data-ttu-id="a5824-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5824-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a5824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5824-102">SYNOPSIS</span></span>
<span data-ttu-id="a5824-103">Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="a5824-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a5824-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5824-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5824-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5824-105">DESCRIPTION</span></span>
<span data-ttu-id="a5824-106">**Add-AzDataLakeStoreVirtualNetworkRule** cmdlet 'ı belirtilen Data Lake Store hesabına bir sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="a5824-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a5824-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5824-107">EXAMPLES</span></span>

### <span data-ttu-id="a5824-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5824-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="a5824-109">Bu, alt ağ kimliği "DLS" hesabında "myVNET" adlı yeni bir sanal ağ kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="a5824-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="a5824-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5824-110">PARAMETERS</span></span>

### <span data-ttu-id="a5824-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a5824-111">-Account</span></span>
<span data-ttu-id="a5824-112">Sanal ağ kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="a5824-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="a5824-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5824-113">-DefaultProfile</span></span>
<span data-ttu-id="a5824-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5824-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5824-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5824-115">-Name</span></span>
<span data-ttu-id="a5824-116">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="a5824-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a5824-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a5824-117">-SubnetId</span></span>
<span data-ttu-id="a5824-118">Sanal ağ kuralının alt NetID değeri</span><span class="sxs-lookup"><span data-stu-id="a5824-118">The subnetId of the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5824-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5824-119">-Confirm</span></span>
<span data-ttu-id="a5824-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5824-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5824-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5824-121">-WhatIf</span></span>
<span data-ttu-id="a5824-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5824-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5824-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5824-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5824-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5824-124">CommonParameters</span></span>
<span data-ttu-id="a5824-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5824-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5824-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5824-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5824-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5824-127">INPUTS</span></span>

### <span data-ttu-id="a5824-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5824-128">System.String</span></span>

## <span data-ttu-id="a5824-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5824-129">OUTPUTS</span></span>

### <span data-ttu-id="a5824-130">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5824-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a5824-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5824-131">NOTES</span></span>

## <span data-ttu-id="a5824-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5824-132">RELATED LINKS</span></span>
