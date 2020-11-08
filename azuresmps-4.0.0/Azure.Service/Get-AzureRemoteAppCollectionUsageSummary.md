---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106330"
---
# <span data-ttu-id="28bb1-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="28bb1-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="28bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="28bb1-103">Azure RemoteApp koleksiyonu için kullanım özetini alır.</span><span class="sxs-lookup"><span data-stu-id="28bb1-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="28bb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28bb1-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28bb1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="28bb1-106">**Get-AzureRemoteAppCollectionUsageSummary** cmdlet 'ı bir Azure RemoteApp koleksiyonu için kullanım özetini alır.</span><span class="sxs-lookup"><span data-stu-id="28bb1-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="28bb1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="28bb1-108">Örnek 1: Kullanım Özeti alma</span><span class="sxs-lookup"><span data-stu-id="28bb1-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="28bb1-109">Bu komut, contoso adlı bir koleksiyon için 2014 yılında Aralık ayının kullanım özetini alır.</span><span class="sxs-lookup"><span data-stu-id="28bb1-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="28bb1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28bb1-110">PARAMETERS</span></span>

### <span data-ttu-id="28bb1-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="28bb1-111">-CollectionName</span></span>
<span data-ttu-id="28bb1-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bb1-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28bb1-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="28bb1-113">-Profile</span></span>
<span data-ttu-id="28bb1-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bb1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28bb1-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="28bb1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28bb1-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="28bb1-116">-UsageMonth</span></span>
<span data-ttu-id="28bb1-117">Bir kullanım özetinin alınacağı ay için iki basamaklı bir sayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bb1-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="28bb1-118">Bu parametre belirtilmezse, bu cmdlet geçerli ay için kullanım sağlar.</span><span class="sxs-lookup"><span data-stu-id="28bb1-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28bb1-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="28bb1-119">-UsageYear</span></span>
<span data-ttu-id="28bb1-120">Kullanım özetinin alınacağı dört haneli yılı belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bb1-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="28bb1-121">Bu parametre belirtilmemişse, bu cmdlet geçerli yıl için kullanım özetini sağlar.</span><span class="sxs-lookup"><span data-stu-id="28bb1-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28bb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28bb1-122">CommonParameters</span></span>
<span data-ttu-id="28bb1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28bb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28bb1-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28bb1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28bb1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28bb1-125">INPUTS</span></span>

## <span data-ttu-id="28bb1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28bb1-126">OUTPUTS</span></span>

## <span data-ttu-id="28bb1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28bb1-127">NOTES</span></span>

## <span data-ttu-id="28bb1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28bb1-128">RELATED LINKS</span></span>

[<span data-ttu-id="28bb1-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="28bb1-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="28bb1-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="28bb1-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


