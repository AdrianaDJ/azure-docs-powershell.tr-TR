---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106428"
---
# <span data-ttu-id="c44f4-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c44f4-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="c44f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c44f4-102">SYNOPSIS</span></span>

<span data-ttu-id="c44f4-103">Otomasyon sertifikasının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="c44f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c44f4-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c44f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c44f4-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c44f4-106">**Set-AzureAutomationCertificate** cmdlet 'ı, Microsoft Azure Otomasyonu 'nda bir sertifikanın yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="c44f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c44f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c44f4-108">Örnek 1: sertifikayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c44f4-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="c44f4-109">Bu komutlar, Otomasyon 'daki MyCertificate adlı sertifikayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="c44f4-110">İlk komut, sertifikayı güncelleştiren ikinci komutta kullanılan sertifika dosyasının parolasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c44f4-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="c44f4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c44f4-111">PARAMETERS</span></span>

### <span data-ttu-id="c44f4-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c44f4-112">-AutomationAccountName</span></span>
<span data-ttu-id="c44f4-113">Sertifikayla birlikte Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-113">Specifies the name of the Automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c44f4-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c44f4-114">-Description</span></span>
<span data-ttu-id="c44f4-115">Sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="c44f4-116">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="c44f4-116">-Exportable</span></span>
<span data-ttu-id="c44f4-117">Sertifikanın dışarı aktarılaabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c44f4-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c44f4-118">-Name</span></span>
<span data-ttu-id="c44f4-119">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-119">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c44f4-120">-Parola</span><span class="sxs-lookup"><span data-stu-id="c44f4-120">-Password</span></span>
<span data-ttu-id="c44f4-121">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-121">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c44f4-122">-Yol</span><span class="sxs-lookup"><span data-stu-id="c44f4-122">-Path</span></span>
<span data-ttu-id="c44f4-123">Karşıya yüklenecek bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="c44f4-124">Dosya. cer veya. pfx olabilir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="c44f4-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="c44f4-125">-Profile</span></span>
<span data-ttu-id="c44f4-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c44f4-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c44f4-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c44f4-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c44f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44f4-128">CommonParameters</span></span>
<span data-ttu-id="c44f4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c44f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44f4-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44f4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c44f4-131">INPUTS</span></span>

## <span data-ttu-id="c44f4-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c44f4-132">OUTPUTS</span></span>

### <span data-ttu-id="c44f4-133">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="c44f4-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="c44f4-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c44f4-134">NOTES</span></span>

## <span data-ttu-id="c44f4-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c44f4-135">RELATED LINKS</span></span>

[<span data-ttu-id="c44f4-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c44f4-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="c44f4-137">Yeni-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c44f4-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="c44f4-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c44f4-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


