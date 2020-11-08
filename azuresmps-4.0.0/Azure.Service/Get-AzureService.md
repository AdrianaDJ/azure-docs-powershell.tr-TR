---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106309"
---
# <span data-ttu-id="e700f-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="e700f-101">Get-AzureService</span></span>

## <span data-ttu-id="e700f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e700f-102">SYNOPSIS</span></span>
<span data-ttu-id="e700f-103">Geçerli aboneliğin bulut hizmetleri hakkında bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e700f-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="e700f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e700f-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e700f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e700f-105">DESCRIPTION</span></span>
<span data-ttu-id="e700f-106">**Get-AzureService** cmdlet 'i geçerli abonelikle Ilişkilendirilmiş tüm Azure bulut hizmetlerini içeren bir liste nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e700f-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="e700f-107">*HizmetAdı* parametresini belirtirseniz, **Get-AzureService** yalnızca eşleşen hizmette bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e700f-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="e700f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e700f-108">EXAMPLES</span></span>

### <span data-ttu-id="e700f-109">Örnek 1: tüm hizmetler hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="e700f-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="e700f-110">Bu komut, geçerli abonelikle ilişkilendirilmiş tüm Azure hizmetleri hakkında bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e700f-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="e700f-111">Örnek 2: belirtilen hizmet hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e700f-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="e700f-112">Bu komut $MySvc hizmeti hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e700f-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="e700f-113">Örnek 3: kullanılabilir yöntemleri ve özellikleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e700f-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="e700f-114">Bu komut **Get-AzureService** cmdlet 'inde sağlanan özellikleri ve yöntemleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e700f-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="e700f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e700f-115">PARAMETERS</span></span>

### <span data-ttu-id="e700f-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e700f-116">-InformationAction</span></span>
<span data-ttu-id="e700f-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e700f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e700f-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e700f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e700f-119">'A</span><span class="sxs-lookup"><span data-stu-id="e700f-119">Continue</span></span>
- <span data-ttu-id="e700f-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="e700f-120">Ignore</span></span>
- <span data-ttu-id="e700f-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e700f-121">Inquire</span></span>
- <span data-ttu-id="e700f-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e700f-122">SilentlyContinue</span></span>
- <span data-ttu-id="e700f-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e700f-123">Stop</span></span>
- <span data-ttu-id="e700f-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e700f-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e700f-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e700f-125">-InformationVariable</span></span>
<span data-ttu-id="e700f-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e700f-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e700f-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="e700f-127">-Profile</span></span>
<span data-ttu-id="e700f-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e700f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e700f-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e700f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e700f-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e700f-130">-ServiceName</span></span>
<span data-ttu-id="e700f-131">Bilgilerin geri döndürülmesi gereken hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e700f-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e700f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e700f-132">CommonParameters</span></span>
<span data-ttu-id="e700f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e700f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e700f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e700f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e700f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e700f-135">INPUTS</span></span>

## <span data-ttu-id="e700f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e700f-136">OUTPUTS</span></span>

### <span data-ttu-id="e700f-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="e700f-137">HostedServiceContext</span></span>

## <span data-ttu-id="e700f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e700f-138">NOTES</span></span>

## <span data-ttu-id="e700f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e700f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e700f-140">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="e700f-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="e700f-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="e700f-141">Set-AzureService</span></span>](./Set-AzureService.md)


