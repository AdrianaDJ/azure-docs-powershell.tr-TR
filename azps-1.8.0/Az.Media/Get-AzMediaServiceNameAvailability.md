---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: 8c62bf114feee8f9b87e2b7ca35b4c67b423ed66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915767"
---
# <span data-ttu-id="31e7c-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="31e7c-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="31e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="31e7c-103">Medya hizmeti adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="31e7c-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="31e7c-104">Medya hizmeti adları genel olarak benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="31e7c-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="31e7c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31e7c-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="31e7c-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="31e7c-106">DESCRIPTION</span></span>
<span data-ttu-id="31e7c-107">**Get-Azmediaservicenameuygunluk** cmdlet 'i bir medya hizmeti adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="31e7c-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="31e7c-108">Medya hizmeti adları genel olarak benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="31e7c-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="31e7c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="31e7c-110">Örnek 1: medya hizmeti adının kullanılabilir olup olmadığını denetleme</span><span class="sxs-lookup"><span data-stu-id="31e7c-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="31e7c-111">Bu komut, MediaService1 ad olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="31e7c-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="31e7c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="31e7c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31e7c-113">-AccountName</span></span>
<span data-ttu-id="31e7c-114">Bu cmdlet 'in aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e7c-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="31e7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e7c-115">-DefaultProfile</span></span>
<span data-ttu-id="31e7c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="31e7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31e7c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e7c-117">CommonParameters</span></span>
<span data-ttu-id="31e7c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31e7c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e7c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e7c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e7c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31e7c-120">INPUTS</span></span>

### <span data-ttu-id="31e7c-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="31e7c-121">None</span></span>

## <span data-ttu-id="31e7c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31e7c-122">OUTPUTS</span></span>

### <span data-ttu-id="31e7c-123">Microsoft. Azure. Commands. Media. modeller. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="31e7c-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="31e7c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31e7c-124">NOTES</span></span>

## <span data-ttu-id="31e7c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31e7c-125">RELATED LINKS</span></span>

[<span data-ttu-id="31e7c-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="31e7c-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="31e7c-127">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="31e7c-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="31e7c-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="31e7c-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="31e7c-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="31e7c-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


