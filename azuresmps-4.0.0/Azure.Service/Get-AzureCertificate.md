---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106356"
---
# <span data-ttu-id="9ab7d-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9ab7d-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="9ab7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ab7d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab7d-103">Bir Azure hizmetinden sertifika nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="9ab7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ab7d-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ab7d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ab7d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab7d-106">**Get-Azurecercertificate** . cmdlet 'ı bir Azure hizmetinden sertifika nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="9ab7d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ab7d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ab7d-108">Örnek 1: hizmetten sertifikaları alma</span><span class="sxs-lookup"><span data-stu-id="9ab7d-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="9ab7d-109">Bu komut, ContosoService adlı hizmetten sertifika nesnelerini alır ve $AzureCert değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="9ab7d-110">Örnek 2: hizmetten sertifika alma</span><span class="sxs-lookup"><span data-stu-id="9ab7d-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="9ab7d-111">Bu komut, ContosoService adlı hizmetten belirtilen parmak iziyle tanımlanan sertifika nesnesini alır ve $AzureCert değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="9ab7d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ab7d-112">PARAMETERS</span></span>

### <span data-ttu-id="9ab7d-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9ab7d-113">-InformationAction</span></span>
<span data-ttu-id="9ab7d-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9ab7d-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9ab7d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ab7d-116">'A</span><span class="sxs-lookup"><span data-stu-id="9ab7d-116">Continue</span></span>
- <span data-ttu-id="9ab7d-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="9ab7d-117">Ignore</span></span>
- <span data-ttu-id="9ab7d-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9ab7d-118">Inquire</span></span>
- <span data-ttu-id="9ab7d-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9ab7d-119">SilentlyContinue</span></span>
- <span data-ttu-id="9ab7d-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9ab7d-120">Stop</span></span>
- <span data-ttu-id="9ab7d-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9ab7d-121">Suspend</span></span>

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

### <span data-ttu-id="9ab7d-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9ab7d-122">-InformationVariable</span></span>
<span data-ttu-id="9ab7d-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9ab7d-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="9ab7d-124">-Profile</span></span>
<span data-ttu-id="9ab7d-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ab7d-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ab7d-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="9ab7d-127">-ServiceName</span></span>
<span data-ttu-id="9ab7d-128">Bu cmdlet 'in sertifika aldığı Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab7d-129">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="9ab7d-129">-Thumbprint</span></span>
<span data-ttu-id="9ab7d-130">Bu cmdlet 'in aldığı sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab7d-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9ab7d-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="9ab7d-132">Sertifika parmak izini oluşturmak için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab7d-133">CommonParameters</span></span>
<span data-ttu-id="9ab7d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ab7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab7d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab7d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab7d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ab7d-136">INPUTS</span></span>

## <span data-ttu-id="9ab7d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ab7d-137">OUTPUTS</span></span>

### <span data-ttu-id="9ab7d-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="9ab7d-138">CertificateContext</span></span>

## <span data-ttu-id="9ab7d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ab7d-139">NOTES</span></span>

## <span data-ttu-id="9ab7d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ab7d-140">RELATED LINKS</span></span>

[<span data-ttu-id="9ab7d-141">Add-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="9ab7d-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="9ab7d-142">New-Azurecercertificate Atesetting</span><span class="sxs-lookup"><span data-stu-id="9ab7d-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="9ab7d-143">Remove-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="9ab7d-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


