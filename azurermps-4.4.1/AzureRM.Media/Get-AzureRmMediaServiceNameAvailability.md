---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763701"
---
# <span data-ttu-id="8727a-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8727a-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="8727a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8727a-102">SYNOPSIS</span></span>
<span data-ttu-id="8727a-103">Medya hizmeti adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="8727a-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="8727a-104">Medya hizmeti adları genel olarak benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="8727a-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8727a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8727a-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="8727a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8727a-106">DESCRIPTION</span></span>
<span data-ttu-id="8727a-107">**Get-Azurermmediaservicenameuygunluk** cmdlet 'i bir medya hizmeti adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="8727a-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="8727a-108">Medya hizmeti adları genel olarak benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="8727a-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="8727a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8727a-109">EXAMPLES</span></span>

### <span data-ttu-id="8727a-110">Örnek 1: medya hizmeti adının kullanılabilir olup olmadığını denetleme</span><span class="sxs-lookup"><span data-stu-id="8727a-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="8727a-111">Bu komut, MediaService1 ad olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="8727a-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="8727a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8727a-112">PARAMETERS</span></span>

### <span data-ttu-id="8727a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8727a-113">-AccountName</span></span>
<span data-ttu-id="8727a-114">Bu cmdlet 'in aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8727a-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8727a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8727a-115">-DefaultProfile</span></span>
<span data-ttu-id="8727a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8727a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8727a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8727a-117">CommonParameters</span></span>
<span data-ttu-id="8727a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8727a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8727a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8727a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8727a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8727a-120">INPUTS</span></span>

## <span data-ttu-id="8727a-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8727a-121">OUTPUTS</span></span>

### <span data-ttu-id="8727a-122">Microsoft. Azure. Commands. Media. modeller. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="8727a-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="8727a-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8727a-123">NOTES</span></span>

## <span data-ttu-id="8727a-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8727a-124">RELATED LINKS</span></span>

[<span data-ttu-id="8727a-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8727a-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="8727a-126">Yeni-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8727a-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="8727a-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8727a-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="8727a-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8727a-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


