---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593809"
---
# <span data-ttu-id="a8b96-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a8b96-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="a8b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8b96-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b96-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8b96-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8b96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8b96-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8b96-105">DESCRIPTION</span></span>
<span data-ttu-id="a8b96-106">**Remove-AzureRmRelayNamespace** cmdlet 'i belirtilen kaynak grubundaki ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8b96-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="a8b96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8b96-107">EXAMPLES</span></span>

### <span data-ttu-id="a8b96-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8b96-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="a8b96-109">Belirtilen kaynak grubundan geçiş ad alanını kaldırır `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="a8b96-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="a8b96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8b96-110">PARAMETERS</span></span>

### <span data-ttu-id="a8b96-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8b96-111">-Name</span></span>
<span data-ttu-id="a8b96-112">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a8b96-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a8b96-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b96-113">-ResourceGroupName</span></span>
<span data-ttu-id="a8b96-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a8b96-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="a8b96-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8b96-115">-Confirm</span></span>
<span data-ttu-id="a8b96-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8b96-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b96-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b96-117">-WhatIf</span></span>
<span data-ttu-id="a8b96-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8b96-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8b96-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8b96-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b96-120">-DefaultProfile</span></span>
<span data-ttu-id="a8b96-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8b96-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8b96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b96-122">CommonParameters</span></span>
<span data-ttu-id="a8b96-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8b96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b96-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b96-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b96-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8b96-125">INPUTS</span></span>

### <span data-ttu-id="a8b96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b96-126">-ResourceGroupName</span></span>
 <span data-ttu-id="a8b96-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a8b96-127">System.String</span></span>

### <span data-ttu-id="a8b96-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8b96-128">-Name</span></span>
 <span data-ttu-id="a8b96-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a8b96-129">System.String</span></span>

## <span data-ttu-id="a8b96-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8b96-130">OUTPUTS</span></span>

### <span data-ttu-id="a8b96-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8b96-131">System.Object</span></span>

## <span data-ttu-id="a8b96-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8b96-132">NOTES</span></span>

## <span data-ttu-id="a8b96-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8b96-133">RELATED LINKS</span></span>
