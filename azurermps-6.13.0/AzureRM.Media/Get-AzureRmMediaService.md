---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 76705a699b814bf52d7c874ec86e067735764936
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589512"
---
# <span data-ttu-id="4ebc6-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4ebc6-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="4ebc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ebc6-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebc6-103">Medya hizmeti hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ebc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ebc6-104">SYNTAX</span></span>

### <span data-ttu-id="4ebc6-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ebc6-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebc6-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ebc6-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ebc6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ebc6-107">DESCRIPTION</span></span>
<span data-ttu-id="4ebc6-108">**Get-AzureRmMediaService** cmdlet 'i medya hizmeti hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="4ebc6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ebc6-109">EXAMPLES</span></span>

### <span data-ttu-id="4ebc6-110">Örnek 1: kaynak grubundaki tüm medya hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="4ebc6-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="4ebc6-111">Bu komut, ResourceGroup001 adlı kaynak grubundaki tüm medya hizmetlerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="4ebc6-112">Örnek 2: medya hizmeti özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="4ebc6-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="4ebc6-113">Bu komut, MediaService1 adındaki kaynak grubuna ait olan medya hizmeti özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="4ebc6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ebc6-114">PARAMETERS</span></span>

### <span data-ttu-id="4ebc6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ebc6-115">-AccountName</span></span>
<span data-ttu-id="4ebc6-116">Bu cmdlet 'in aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4ebc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebc6-117">-DefaultProfile</span></span>
<span data-ttu-id="4ebc6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4ebc6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ebc6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebc6-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ebc6-120">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="4ebc6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebc6-121">CommonParameters</span></span>
<span data-ttu-id="4ebc6-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ebc6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebc6-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebc6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebc6-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ebc6-124">INPUTS</span></span>

### <span data-ttu-id="4ebc6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebc6-125">System.String</span></span>

## <span data-ttu-id="4ebc6-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ebc6-126">OUTPUTS</span></span>

### <span data-ttu-id="4ebc6-127">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="4ebc6-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="4ebc6-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ebc6-128">NOTES</span></span>

## <span data-ttu-id="4ebc6-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ebc6-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ebc6-130">Yeni-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4ebc6-130">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="4ebc6-131">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4ebc6-131">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="4ebc6-132">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4ebc6-132">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


