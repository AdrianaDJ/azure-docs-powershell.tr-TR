---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268985"
---
# <span data-ttu-id="f0b6c-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f0b6c-101">Get-AzMediaService</span></span>

## <span data-ttu-id="f0b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b6c-103">Medya hizmeti hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-103">Gets information about a media service.</span></span>

## <span data-ttu-id="f0b6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0b6c-104">SYNTAX</span></span>

### <span data-ttu-id="f0b6c-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b6c-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0b6c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b6c-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0b6c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="f0b6c-108">**Get-AzMediaService** cmdlet 'i medya hizmeti hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="f0b6c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b6c-110">Örnek 1: kaynak grubundaki tüm medya hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="f0b6c-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="f0b6c-111">Bu komut, ResourceGroup001 adlı kaynak grubundaki tüm medya hizmetlerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f0b6c-112">Örnek 2: medya hizmeti özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="f0b6c-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="f0b6c-113">Bu komut, MediaService1 adındaki kaynak grubuna ait olan medya hizmeti özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f0b6c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0b6c-114">PARAMETERS</span></span>

### <span data-ttu-id="f0b6c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0b6c-115">-AccountName</span></span>
<span data-ttu-id="f0b6c-116">Bu cmdlet 'in aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b6c-117">-DefaultProfile</span></span>
<span data-ttu-id="f0b6c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f0b6c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0b6c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b6c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0b6c-120">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f0b6c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b6c-121">CommonParameters</span></span>
<span data-ttu-id="f0b6c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0b6c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b6c-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b6c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b6c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0b6c-124">INPUTS</span></span>

### <span data-ttu-id="f0b6c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f0b6c-125">System.String</span></span>

## <span data-ttu-id="f0b6c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0b6c-126">OUTPUTS</span></span>

### <span data-ttu-id="f0b6c-127">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="f0b6c-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f0b6c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0b6c-128">NOTES</span></span>

## <span data-ttu-id="f0b6c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0b6c-129">RELATED LINKS</span></span>

[<span data-ttu-id="f0b6c-130">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f0b6c-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="f0b6c-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f0b6c-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f0b6c-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f0b6c-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


