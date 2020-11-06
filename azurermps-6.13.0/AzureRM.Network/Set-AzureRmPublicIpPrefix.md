---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572698"
---
# <span data-ttu-id="91cd0-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91cd0-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="91cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="91cd0-103">Var olan Publicıpprefix için etiketleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="91cd0-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91cd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91cd0-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91cd0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="91cd0-106">**Set-AzureRmPublicIpPrefix** cmdlet 'ı genel IP önekinin etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="91cd0-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="91cd0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="91cd0-108">Genel IP öneki için etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="91cd0-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="91cd0-109">İlk komut mevcut bir genel IP önekini alır, ikinci komut Etiketler özelliğini ayarlar ve üçüncü komut varolan nesneyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="91cd0-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="91cd0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91cd0-110">PARAMETERS</span></span>

### <span data-ttu-id="91cd0-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="91cd0-111">-AsJob</span></span>
<span data-ttu-id="91cd0-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="91cd0-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cd0-113">-DefaultProfile</span></span>
<span data-ttu-id="91cd0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91cd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91cd0-115">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="91cd0-115">-PublicIpPrefix</span></span>
<span data-ttu-id="91cd0-116">Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="91cd0-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91cd0-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="91cd0-117">-Confirm</span></span>
<span data-ttu-id="91cd0-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91cd0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cd0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91cd0-119">-WhatIf</span></span>
<span data-ttu-id="91cd0-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91cd0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91cd0-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91cd0-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cd0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cd0-122">CommonParameters</span></span>
<span data-ttu-id="91cd0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91cd0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="91cd0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cd0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cd0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91cd0-125">INPUTS</span></span>

### <span data-ttu-id="91cd0-126">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91cd0-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="91cd0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91cd0-127">OUTPUTS</span></span>

### <span data-ttu-id="91cd0-128">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91cd0-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="91cd0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91cd0-129">NOTES</span></span>

## <span data-ttu-id="91cd0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91cd0-130">RELATED LINKS</span></span>
