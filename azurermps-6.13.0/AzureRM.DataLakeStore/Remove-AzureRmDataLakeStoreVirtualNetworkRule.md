---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762956"
---
# <span data-ttu-id="eb970-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="eb970-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="eb970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb970-102">SYNOPSIS</span></span>
<span data-ttu-id="eb970-103">Belirtilen veri Lake Store 'da belirtilen sanal ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb970-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb970-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb970-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb970-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb970-105">DESCRIPTION</span></span>
<span data-ttu-id="eb970-106">**Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet 'ı belirtilen Data Lake Store 'da belirtilen sanal ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb970-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="eb970-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb970-107">EXAMPLES</span></span>

### <span data-ttu-id="eb970-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eb970-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="eb970-109">"MyVNET" sanal ağ kuralını "DLS" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="eb970-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="eb970-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb970-110">PARAMETERS</span></span>

### <span data-ttu-id="eb970-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="eb970-111">-Account</span></span>
<span data-ttu-id="eb970-112">Sanal ağ kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="eb970-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="eb970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb970-113">-DefaultProfile</span></span>
<span data-ttu-id="eb970-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb970-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb970-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb970-115">-Name</span></span>
<span data-ttu-id="eb970-116">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="eb970-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="eb970-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="eb970-117">-PassThru</span></span>
<span data-ttu-id="eb970-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb970-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="eb970-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb970-119">-Confirm</span></span>
<span data-ttu-id="eb970-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb970-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb970-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb970-121">-WhatIf</span></span>
<span data-ttu-id="eb970-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb970-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb970-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb970-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb970-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb970-124">CommonParameters</span></span>
<span data-ttu-id="eb970-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb970-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb970-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb970-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb970-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb970-127">INPUTS</span></span>

### <span data-ttu-id="eb970-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb970-128">System.String</span></span>

### <span data-ttu-id="eb970-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb970-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb970-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb970-130">OUTPUTS</span></span>

### <span data-ttu-id="eb970-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb970-131">System.Boolean</span></span>

## <span data-ttu-id="eb970-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb970-132">NOTES</span></span>

## <span data-ttu-id="eb970-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb970-133">RELATED LINKS</span></span>
