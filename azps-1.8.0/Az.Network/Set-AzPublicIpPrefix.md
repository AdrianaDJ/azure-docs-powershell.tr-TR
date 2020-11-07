---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: caa0baf8e26ea2cec94a59bd2a86e6394b4ade91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759979"
---
# <span data-ttu-id="e84b3-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="e84b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e84b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e84b3-103">Var olan Publicıpprefix için etiketleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="e84b3-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="e84b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e84b3-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e84b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e84b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e84b3-106">**Set-AzPublicIpPrefix** cmdlet 'ı genel IP önekinin etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e84b3-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="e84b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e84b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e84b3-108">Genel IP öneki için etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="e84b3-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="e84b3-109">İlk komut mevcut bir genel IP önekini alır, ikinci komut Etiketler özelliğini ayarlar ve üçüncü komut varolan nesneyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e84b3-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="e84b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e84b3-110">PARAMETERS</span></span>

### <span data-ttu-id="e84b3-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e84b3-111">-AsJob</span></span>
<span data-ttu-id="e84b3-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e84b3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e84b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84b3-113">-DefaultProfile</span></span>
<span data-ttu-id="e84b3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e84b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e84b3-115">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-115">-PublicIpPrefix</span></span>
<span data-ttu-id="e84b3-116">Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e84b3-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="e84b3-117">-Confirm</span></span>
<span data-ttu-id="e84b3-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e84b3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e84b3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e84b3-119">-WhatIf</span></span>
<span data-ttu-id="e84b3-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e84b3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e84b3-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e84b3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e84b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84b3-122">CommonParameters</span></span>
<span data-ttu-id="e84b3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e84b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84b3-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e84b3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84b3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e84b3-125">INPUTS</span></span>

### <span data-ttu-id="e84b3-126">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e84b3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e84b3-127">OUTPUTS</span></span>

### <span data-ttu-id="e84b3-128">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e84b3-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e84b3-129">NOTES</span></span>

## <span data-ttu-id="e84b3-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e84b3-130">RELATED LINKS</span></span>

[<span data-ttu-id="e84b3-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="e84b3-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="e84b3-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e84b3-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)