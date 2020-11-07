---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: a6d1ff6d169fab90fa866e94577ce9b3f9580a4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751387"
---
# <span data-ttu-id="d680b-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d680b-101">Get-AzMediaService</span></span>

## <span data-ttu-id="d680b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d680b-102">SYNOPSIS</span></span>
<span data-ttu-id="d680b-103">Medya hizmeti hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d680b-103">Gets information about a media service.</span></span>

## <span data-ttu-id="d680b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d680b-104">SYNTAX</span></span>

### <span data-ttu-id="d680b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d680b-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d680b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d680b-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d680b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d680b-107">DESCRIPTION</span></span>
<span data-ttu-id="d680b-108">**Get-AzMediaService** cmdlet 'i medya hizmeti hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d680b-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="d680b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d680b-109">EXAMPLES</span></span>

### <span data-ttu-id="d680b-110">Örnek 1: kaynak grubundaki tüm medya hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="d680b-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="d680b-111">Bu komut, ResourceGroup001 adlı kaynak grubundaki tüm medya hizmetlerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="d680b-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="d680b-112">Örnek 2: medya hizmeti özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="d680b-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="d680b-113">Bu komut, MediaService1 adındaki kaynak grubuna ait olan medya hizmeti özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="d680b-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="d680b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d680b-114">PARAMETERS</span></span>

### <span data-ttu-id="d680b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d680b-115">-AccountName</span></span>
<span data-ttu-id="d680b-116">Bu cmdlet 'in aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d680b-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d680b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d680b-117">-DefaultProfile</span></span>
<span data-ttu-id="d680b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d680b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d680b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d680b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d680b-120">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d680b-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d680b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d680b-121">CommonParameters</span></span>
<span data-ttu-id="d680b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d680b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d680b-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d680b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d680b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d680b-124">INPUTS</span></span>

### <span data-ttu-id="d680b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d680b-125">System.String</span></span>

## <span data-ttu-id="d680b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d680b-126">OUTPUTS</span></span>

### <span data-ttu-id="d680b-127">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="d680b-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="d680b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d680b-128">NOTES</span></span>

## <span data-ttu-id="d680b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d680b-129">RELATED LINKS</span></span>

[<span data-ttu-id="d680b-130">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d680b-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="d680b-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d680b-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="d680b-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d680b-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

