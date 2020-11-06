---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589108"
---
# <span data-ttu-id="b05a4-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b05a4-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b05a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b05a4-103">Belirtilen kaynak grubundan bir hizmet veri yolu ad alanının yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b05a4-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b05a4-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b05a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b05a4-105">DESCRIPTION</span></span>
<span data-ttu-id="b05a4-106">**Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet 'i, belirtilen kaynak grubu Için bir hizmet veri yolu ad alanının yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b05a4-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="b05a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b05a4-107">EXAMPLES</span></span>

### <span data-ttu-id="b05a4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b05a4-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="b05a4-109">`SBAuthoRule1`Belirtilen kaynak grubundan ad alanının yetkilendirme kuralını kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b05a4-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="b05a4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b05a4-110">PARAMETERS</span></span>

### <span data-ttu-id="b05a4-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="b05a4-111">-Confirm</span></span>
<span data-ttu-id="b05a4-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b05a4-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b05a4-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05a4-113">-WhatIf</span></span>
<span data-ttu-id="b05a4-114">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b05a4-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b05a4-115">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b05a4-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b05a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05a4-116">-DefaultProfile</span></span>
<span data-ttu-id="b05a4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b05a4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b05a4-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b05a4-118">-Name</span></span>
<span data-ttu-id="b05a4-119">Ad alanı AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="b05a4-119">Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a4-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b05a4-120">-Namespace</span></span>
<span data-ttu-id="b05a4-121">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b05a4-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b05a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b05a4-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b05a4-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05a4-124">CommonParameters</span></span>
<span data-ttu-id="b05a4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b05a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05a4-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05a4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b05a4-127">INPUTS</span></span>

### <span data-ttu-id="b05a4-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b05a4-128">-ResourceGroup</span></span>
 <span data-ttu-id="b05a4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a4-129">System.String</span></span>

### <span data-ttu-id="b05a4-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b05a4-130">-NamespaceName</span></span>
 <span data-ttu-id="b05a4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a4-131">System.String</span></span>

### <span data-ttu-id="b05a4-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b05a4-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b05a4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a4-133">System.String</span></span>

## <span data-ttu-id="b05a4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b05a4-134">OUTPUTS</span></span>

### <span data-ttu-id="b05a4-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b05a4-135">System.Boolean</span></span>

## <span data-ttu-id="b05a4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b05a4-136">NOTES</span></span>

## <span data-ttu-id="b05a4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b05a4-137">RELATED LINKS</span></span>

