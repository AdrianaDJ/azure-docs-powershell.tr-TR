---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106167"
---
# <span data-ttu-id="5a791-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="5a791-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="5a791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a791-102">SYNOPSIS</span></span>
<span data-ttu-id="5a791-103">Azure hizmetinden sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a791-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="5a791-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a791-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a791-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a791-105">DESCRIPTION</span></span>
<span data-ttu-id="5a791-106">**Remove-Azurecercertificate** 'in cmdlet 'ı bir Azure hizmetinden sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a791-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="5a791-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a791-107">EXAMPLES</span></span>

### <span data-ttu-id="5a791-108">Örnek 1: hizmetten sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="5a791-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="5a791-109">Bu komut, belirtilen parmak izine sahip sertifika nesnesini bulut hizmetinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a791-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="5a791-110">Örnek 2: hizmetten tüm sertifikaları kaldırma</span><span class="sxs-lookup"><span data-stu-id="5a791-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="5a791-111">Bu komut, **Get-Azurecercertificate** adlı hizmetten contososervice adındaki tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="5a791-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="5a791-112">Komut, ardışık düzen işlecini kullanarak her sertifikayı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="5a791-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a791-113">Bu cmdlet bulut hizmetinden her sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a791-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="5a791-114">Örnek 3: belirli bir parmak izi algoritmasını kullanan bir hizmetten tüm sertifikaları kaldırma</span><span class="sxs-lookup"><span data-stu-id="5a791-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="5a791-115">Bu komut, SHA1 parmak izi algoritmasını kullanan ContosoService adındaki tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="5a791-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="5a791-116">Komut her sertifikayı geçerli cmdlet 'e geçirir ve her sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="5a791-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="5a791-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a791-117">PARAMETERS</span></span>

### <span data-ttu-id="5a791-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5a791-118">-InformationAction</span></span>
<span data-ttu-id="5a791-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a791-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5a791-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5a791-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a791-121">'A</span><span class="sxs-lookup"><span data-stu-id="5a791-121">Continue</span></span>
- <span data-ttu-id="5a791-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="5a791-122">Ignore</span></span>
- <span data-ttu-id="5a791-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="5a791-123">Inquire</span></span>
- <span data-ttu-id="5a791-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="5a791-124">SilentlyContinue</span></span>
- <span data-ttu-id="5a791-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="5a791-125">Stop</span></span>
- <span data-ttu-id="5a791-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="5a791-126">Suspend</span></span>

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

### <span data-ttu-id="5a791-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="5a791-127">-InformationVariable</span></span>
<span data-ttu-id="5a791-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a791-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5a791-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="5a791-129">-Profile</span></span>
<span data-ttu-id="5a791-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a791-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a791-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5a791-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a791-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="5a791-132">-ServiceName</span></span>
<span data-ttu-id="5a791-133">Bu cmdlet 'in sertifikayı kaldırdığı Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a791-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="5a791-134">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="5a791-134">-Thumbprint</span></span>
<span data-ttu-id="5a791-135">Bu cmdlet 'in kaldırdığı sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a791-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a791-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5a791-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="5a791-137">Sertifika parmak izini oluşturmak için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a791-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a791-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a791-138">CommonParameters</span></span>
<span data-ttu-id="5a791-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a791-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a791-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a791-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a791-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a791-141">INPUTS</span></span>

## <span data-ttu-id="5a791-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a791-142">OUTPUTS</span></span>

### <span data-ttu-id="5a791-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="5a791-143">ManagementOperationContext</span></span>

## <span data-ttu-id="5a791-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a791-144">NOTES</span></span>

## <span data-ttu-id="5a791-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a791-145">RELATED LINKS</span></span>

[<span data-ttu-id="5a791-146">Add-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="5a791-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="5a791-147">Get-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="5a791-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="5a791-148">New-Azurecercertificate Atesetting</span><span class="sxs-lookup"><span data-stu-id="5a791-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


