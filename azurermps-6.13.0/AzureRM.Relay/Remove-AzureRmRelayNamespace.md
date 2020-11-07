---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: ac6327176c587bcb221a5ebddbb12ae9adeffbf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764311"
---
# <span data-ttu-id="59824-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="59824-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="59824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59824-102">SYNOPSIS</span></span>
<span data-ttu-id="59824-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59824-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59824-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59824-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59824-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59824-105">DESCRIPTION</span></span>
<span data-ttu-id="59824-106">**Remove-AzureRmRelayNamespace** cmdlet 'i belirtilen kaynak grubundaki ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59824-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="59824-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59824-107">EXAMPLES</span></span>

### <span data-ttu-id="59824-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59824-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="59824-109">Belirtilen kaynak grubundan geçiş ad alanını kaldırır `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="59824-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="59824-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59824-110">PARAMETERS</span></span>

### <span data-ttu-id="59824-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59824-111">-DefaultProfile</span></span>
<span data-ttu-id="59824-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59824-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59824-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="59824-113">-Name</span></span>
<span data-ttu-id="59824-114">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="59824-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="59824-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59824-115">-ResourceGroupName</span></span>
<span data-ttu-id="59824-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="59824-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="59824-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="59824-117">-Confirm</span></span>
<span data-ttu-id="59824-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59824-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59824-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59824-119">-WhatIf</span></span>
<span data-ttu-id="59824-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59824-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59824-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59824-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59824-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59824-122">CommonParameters</span></span>
<span data-ttu-id="59824-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59824-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="59824-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59824-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59824-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59824-125">INPUTS</span></span>

### <span data-ttu-id="59824-126">System. String</span><span class="sxs-lookup"><span data-stu-id="59824-126">System.String</span></span>


## <span data-ttu-id="59824-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59824-127">OUTPUTS</span></span>

### <span data-ttu-id="59824-128">System. void</span><span class="sxs-lookup"><span data-stu-id="59824-128">System.Void</span></span>


## <span data-ttu-id="59824-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59824-129">NOTES</span></span>

## <span data-ttu-id="59824-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59824-130">RELATED LINKS</span></span>
