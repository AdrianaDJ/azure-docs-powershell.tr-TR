---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106579"
---
# <span data-ttu-id="5281a-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="5281a-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="5281a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5281a-102">SYNOPSIS</span></span>
<span data-ttu-id="5281a-103">Azure RemoteApp şablonu görüntüleriyle ilgili bilgileri getirir.</span><span class="sxs-lookup"><span data-stu-id="5281a-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="5281a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5281a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5281a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5281a-105">DESCRIPTION</span></span>
<span data-ttu-id="5281a-106">**Get-Azureremoteapptemplateımage** cmdlet 'ı, Azure RemoteApp şablonu görüntüleriyle Ilgili bilgileri Microsoft Azure 'da alır.</span><span class="sxs-lookup"><span data-stu-id="5281a-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="5281a-107">Bu cmdlet, belirli bir şablon görüntüsü hakkında bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5281a-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="5281a-108">Şablon görüntüsü belirtilmemişse, geçerli abonelikteki tüm şablon resimlerinde yer alan bilgiler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5281a-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="5281a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5281a-109">EXAMPLES</span></span>

### <span data-ttu-id="5281a-110">Örnek 1: tüm şablon görüntülerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="5281a-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="5281a-111">Bu komut, tüm şablon görüntülerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5281a-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="5281a-112">Örnek 2: belirtilen şablon görüntüsü hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="5281a-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="5281a-113">Bu komut, ContosoApps adındaki şablon görüntüsü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5281a-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="5281a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5281a-114">PARAMETERS</span></span>

### <span data-ttu-id="5281a-115">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="5281a-115">-ImageName</span></span>
<span data-ttu-id="5281a-116">Azure RemoteApp şablonu görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5281a-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="5281a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="5281a-117">-Profile</span></span>
<span data-ttu-id="5281a-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5281a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5281a-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5281a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5281a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5281a-120">CommonParameters</span></span>
<span data-ttu-id="5281a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5281a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5281a-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5281a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5281a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5281a-123">INPUTS</span></span>

## <span data-ttu-id="5281a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5281a-124">OUTPUTS</span></span>

## <span data-ttu-id="5281a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5281a-125">NOTES</span></span>

## <span data-ttu-id="5281a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5281a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5281a-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="5281a-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="5281a-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="5281a-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


