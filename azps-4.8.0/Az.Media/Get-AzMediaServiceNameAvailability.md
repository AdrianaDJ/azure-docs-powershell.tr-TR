---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268980"
---
# <span data-ttu-id="11907-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="11907-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="11907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11907-102">SYNOPSIS</span></span>
<span data-ttu-id="11907-103">Medya hizmeti adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="11907-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="11907-104">Medya hizmeti adları genel olarak benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="11907-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="11907-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11907-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="11907-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="11907-106">DESCRIPTION</span></span>
<span data-ttu-id="11907-107">**Get-Azmediaservicenameuygunluk** cmdlet 'i bir medya hizmeti adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="11907-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="11907-108">Medya hizmeti adları genel olarak benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="11907-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="11907-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11907-109">EXAMPLES</span></span>

### <span data-ttu-id="11907-110">Örnek 1: medya hizmeti adının kullanılabilir olup olmadığını denetleme</span><span class="sxs-lookup"><span data-stu-id="11907-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="11907-111">Bu komut, MediaService1 ad olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="11907-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="11907-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11907-112">PARAMETERS</span></span>

### <span data-ttu-id="11907-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11907-113">-AccountName</span></span>
<span data-ttu-id="11907-114">Bu cmdlet 'in aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11907-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11907-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11907-115">-DefaultProfile</span></span>
<span data-ttu-id="11907-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="11907-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11907-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11907-117">CommonParameters</span></span>
<span data-ttu-id="11907-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11907-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11907-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11907-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11907-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11907-120">INPUTS</span></span>

### <span data-ttu-id="11907-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="11907-121">None</span></span>

## <span data-ttu-id="11907-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11907-122">OUTPUTS</span></span>

### <span data-ttu-id="11907-123">Microsoft. Azure. Commands. Media. modeller. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="11907-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="11907-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11907-124">NOTES</span></span>

## <span data-ttu-id="11907-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11907-125">RELATED LINKS</span></span>

[<span data-ttu-id="11907-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11907-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="11907-127">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11907-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="11907-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11907-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="11907-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11907-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


