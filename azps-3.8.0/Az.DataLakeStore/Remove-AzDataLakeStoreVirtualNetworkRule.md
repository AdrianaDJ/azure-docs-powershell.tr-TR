---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105040"
---
# <span data-ttu-id="7e312-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7e312-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="7e312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e312-102">SYNOPSIS</span></span>
<span data-ttu-id="7e312-103">Belirtilen veri Lake Store 'da belirtilen sanal ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e312-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7e312-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e312-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e312-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e312-105">DESCRIPTION</span></span>
<span data-ttu-id="7e312-106">**Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet 'ı belirtilen Data Lake Store 'da belirtilen sanal ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e312-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7e312-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e312-107">EXAMPLES</span></span>

### <span data-ttu-id="7e312-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e312-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="7e312-109">"MyVNET" sanal ağ kuralını "DLS" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="7e312-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="7e312-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e312-110">PARAMETERS</span></span>

### <span data-ttu-id="7e312-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="7e312-111">-Account</span></span>
<span data-ttu-id="7e312-112">Sanal ağ kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7e312-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="7e312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e312-113">-DefaultProfile</span></span>
<span data-ttu-id="7e312-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e312-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e312-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e312-115">-Name</span></span>
<span data-ttu-id="7e312-116">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="7e312-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="7e312-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7e312-117">-PassThru</span></span>
<span data-ttu-id="7e312-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e312-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="7e312-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e312-119">-Confirm</span></span>
<span data-ttu-id="7e312-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e312-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e312-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e312-121">-WhatIf</span></span>
<span data-ttu-id="7e312-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e312-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e312-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e312-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e312-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e312-124">CommonParameters</span></span>
<span data-ttu-id="7e312-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e312-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e312-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e312-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e312-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e312-127">INPUTS</span></span>

### <span data-ttu-id="7e312-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7e312-128">System.String</span></span>

## <span data-ttu-id="7e312-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e312-129">OUTPUTS</span></span>

### <span data-ttu-id="7e312-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e312-130">System.Boolean</span></span>

## <span data-ttu-id="7e312-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e312-131">NOTES</span></span>

## <span data-ttu-id="7e312-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e312-132">RELATED LINKS</span></span>
