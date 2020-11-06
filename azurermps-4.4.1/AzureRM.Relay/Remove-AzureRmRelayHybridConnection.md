---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7f65f77d9d1f525dd8850c6934263b608d241751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593021"
---
# <span data-ttu-id="18c6c-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="18c6c-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="18c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="18c6c-103">Belirtilen HybridConnection ad alanından HybridConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18c6c-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18c6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18c6c-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18c6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="18c6c-106">**Remove-AzureRmRelayHybridConnection** cmdlet 'ı belirtilen geçiş ad alanındaki HybridConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18c6c-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="18c6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18c6c-107">EXAMPLES</span></span>

### <span data-ttu-id="18c6c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18c6c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="18c6c-109">Çalışma alanından HybridConnection öğesini kaldırır `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="18c6c-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="18c6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18c6c-110">PARAMETERS</span></span>

### <span data-ttu-id="18c6c-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="18c6c-111">-Name</span></span>
<span data-ttu-id="18c6c-112">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="18c6c-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="18c6c-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="18c6c-113">-Namespace</span></span>
<span data-ttu-id="18c6c-114">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="18c6c-114">Namespace Name.</span></span>

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

### <span data-ttu-id="18c6c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c6c-115">-ResourceGroupName</span></span>
<span data-ttu-id="18c6c-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="18c6c-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c6c-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="18c6c-117">-Confirm</span></span>
<span data-ttu-id="18c6c-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18c6c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c6c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c6c-119">-WhatIf</span></span>
<span data-ttu-id="18c6c-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18c6c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c6c-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18c6c-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c6c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c6c-122">-DefaultProfile</span></span>
<span data-ttu-id="18c6c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18c6c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18c6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c6c-124">CommonParameters</span></span>
<span data-ttu-id="18c6c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18c6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c6c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c6c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c6c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18c6c-127">INPUTS</span></span>

### <span data-ttu-id="18c6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c6c-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="18c6c-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="18c6c-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="18c6c-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="18c6c-130">-Name</span></span>
    System.String

## <span data-ttu-id="18c6c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18c6c-131">OUTPUTS</span></span>

### <span data-ttu-id="18c6c-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="18c6c-132">System.Object</span></span>

## <span data-ttu-id="18c6c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18c6c-133">NOTES</span></span>

## <span data-ttu-id="18c6c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18c6c-134">RELATED LINKS</span></span>

