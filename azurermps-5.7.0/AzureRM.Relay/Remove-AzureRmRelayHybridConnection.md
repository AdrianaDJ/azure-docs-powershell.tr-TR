---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 872683cbf4e26601ec16f05256f0011b0441127c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763239"
---
# <span data-ttu-id="5e0e9-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="5e0e9-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="5e0e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0e9-103">Belirtilen HybridConnection ad alanından HybridConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e0e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e0e9-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0e9-106">**Remove-AzureRmRelayHybridConnection** cmdlet 'ı belirtilen geçiş ad alanındaki HybridConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="5e0e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e0e9-107">EXAMPLES</span></span>

### <span data-ttu-id="5e0e9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e0e9-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="5e0e9-109">Çalışma alanından HybridConnection öğesini kaldırır `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="5e0e9-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="5e0e9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e0e9-110">PARAMETERS</span></span>

### <span data-ttu-id="5e0e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0e9-111">-DefaultProfile</span></span>
<span data-ttu-id="5e0e9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e0e9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e0e9-113">-Name</span></span>
<span data-ttu-id="5e0e9-114">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e0e9-115">-Namespace</span></span>
<span data-ttu-id="5e0e9-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-116">Namespace Name.</span></span>

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

### <span data-ttu-id="5e0e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e0e9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e0e9-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e0e9-119">-Confirm</span></span>
<span data-ttu-id="5e0e9-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0e9-121">-WhatIf</span></span>
<span data-ttu-id="5e0e9-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0e9-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0e9-124">CommonParameters</span></span>
<span data-ttu-id="5e0e9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e0e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0e9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e0e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0e9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e0e9-127">INPUTS</span></span>

### <span data-ttu-id="5e0e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0e9-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="5e0e9-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e0e9-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="5e0e9-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e0e9-130">-Name</span></span>
    System.String

## <span data-ttu-id="5e0e9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e0e9-131">OUTPUTS</span></span>

### <span data-ttu-id="5e0e9-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="5e0e9-132">System.Object</span></span>

## <span data-ttu-id="5e0e9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e0e9-133">NOTES</span></span>

## <span data-ttu-id="5e0e9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e0e9-134">RELATED LINKS</span></span>
