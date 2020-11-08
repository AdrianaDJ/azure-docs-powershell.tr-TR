---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106329"
---
# <span data-ttu-id="fd7c1-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fd7c1-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="fd7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7c1-103">Azure RemoteApp koleksiyonu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="fd7c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd7c1-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd7c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7c1-106">**Get-AzureRemoteAppCollection** cmdlet 'ı, Microsoft Azure 'Daki Azure RemoteApp koleksiyonlarıyla ilgili bilgileri getirir.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="fd7c1-107">Belirli bir koleksiyonda bilgi içeren bir nesne veya geçerli abonelikteki tüm koleksiyonlar için hiçbir koleksiyon belirtilmemişse bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="fd7c1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd7c1-108">EXAMPLES</span></span>

### <span data-ttu-id="fd7c1-109">Örnek 1: tüm koleksiyonların listesini alma</span><span class="sxs-lookup"><span data-stu-id="fd7c1-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="fd7c1-110">Bu komut, abonelikteki tüm Azure RemoteApp koleksiyonlarının bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="fd7c1-111">Örnek 2: belirtilen koleksiyon hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="fd7c1-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="fd7c1-112">Bu komut, ContosoApps adlı Azure RemoteApp koleksiyonu hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="fd7c1-113">Örnek 3: joker karakter kullanarak koleksiyonların listesini alma</span><span class="sxs-lookup"><span data-stu-id="fd7c1-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="fd7c1-114">Bu komut, finans \* ile eşleşen tüm Azure RemoteApp koleksiyonlarının bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="fd7c1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd7c1-115">PARAMETERS</span></span>

### <span data-ttu-id="fd7c1-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="fd7c1-116">-CollectionName</span></span>
<span data-ttu-id="fd7c1-117">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fd7c1-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd7c1-118">-Profile</span></span>
<span data-ttu-id="fd7c1-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd7c1-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd7c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7c1-121">CommonParameters</span></span>
<span data-ttu-id="fd7c1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7c1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7c1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7c1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd7c1-124">INPUTS</span></span>

## <span data-ttu-id="fd7c1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd7c1-125">OUTPUTS</span></span>

## <span data-ttu-id="fd7c1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd7c1-126">NOTES</span></span>

## <span data-ttu-id="fd7c1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd7c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="fd7c1-128">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fd7c1-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="fd7c1-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fd7c1-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="fd7c1-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fd7c1-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="fd7c1-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fd7c1-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


