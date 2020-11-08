---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105632"
---
# <span data-ttu-id="09818-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="09818-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="09818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09818-102">SYNOPSIS</span></span>
<span data-ttu-id="09818-103">Azure RemoteApp koleksiyonunun kullanım ayrıntılarını getirir.</span><span class="sxs-lookup"><span data-stu-id="09818-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="09818-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09818-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="09818-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09818-105">DESCRIPTION</span></span>
<span data-ttu-id="09818-106">**Get-AzureRemoteAppCollectionUsageDetails** cmdlet 'ı bir Azure RemoteApp koleksiyonunun kullanım ayrıntılarını getirir.</span><span class="sxs-lookup"><span data-stu-id="09818-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="09818-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09818-107">EXAMPLES</span></span>

### <span data-ttu-id="09818-108">Örnek 1: koleksiyon için kullanım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="09818-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="09818-109">Bu komut, contoso adlı bir Azure RemoteApp koleksiyonu için 2014 yılında Aralık ayının kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="09818-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="09818-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09818-110">PARAMETERS</span></span>

### <span data-ttu-id="09818-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="09818-111">-AsJob</span></span>
<span data-ttu-id="09818-112">Cmdlet 'in arka planda Windows PowerShell işi olarak çalıştığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09818-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

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

### <span data-ttu-id="09818-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="09818-113">-CollectionName</span></span>
<span data-ttu-id="09818-114">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09818-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="09818-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="09818-115">-Profile</span></span>
<span data-ttu-id="09818-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09818-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="09818-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="09818-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="09818-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="09818-118">-UsageMonth</span></span>
<span data-ttu-id="09818-119">Kullanım ayrıntılarının alınacağı ay için iki basamaklı bir sayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="09818-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="09818-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="09818-120">-UsageYear</span></span>
<span data-ttu-id="09818-121">Kullanım ayrıntılarının alınacağı dört haneli yılı belirtir.</span><span class="sxs-lookup"><span data-stu-id="09818-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="09818-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09818-122">CommonParameters</span></span>
<span data-ttu-id="09818-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09818-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09818-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09818-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09818-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09818-125">INPUTS</span></span>

## <span data-ttu-id="09818-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09818-126">OUTPUTS</span></span>

## <span data-ttu-id="09818-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09818-127">NOTES</span></span>

## <span data-ttu-id="09818-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09818-128">RELATED LINKS</span></span>

[<span data-ttu-id="09818-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="09818-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="09818-130">Get-Azureremoteappizusagesummary</span><span class="sxs-lookup"><span data-stu-id="09818-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


