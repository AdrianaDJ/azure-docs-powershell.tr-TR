---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106222"
---
# <span data-ttu-id="cb7ab-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7ab-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="cb7ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7ab-102">SYNOPSIS</span></span>

<span data-ttu-id="cb7ab-103">Azure Otomasyonu sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="cb7ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb7ab-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cb7ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb7ab-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cb7ab-106">**New-AzureAutomationCertificate** cmdlet 'ı Microsoft Azure Otomasyonu 'nda bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="cb7ab-107">Karşıya yüklenecek sertifika dosyasının yolunu sağlarsınız.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="cb7ab-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb7ab-108">EXAMPLES</span></span>

### <span data-ttu-id="cb7ab-109">Örnek 1: sertifika oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb7ab-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="cb7ab-110">Bu komutlar, MyCertificate adlı Azure Otomasyonu 'nda sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="cb7ab-111">İlk komut, sertifikayı oluşturan ikinci komutta kullanılan sertifika dosyasının parolasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="cb7ab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb7ab-112">PARAMETERS</span></span>

### <span data-ttu-id="cb7ab-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb7ab-113">-AutomationAccountName</span></span>
<span data-ttu-id="cb7ab-114">Sertifikanın saklanacağı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="cb7ab-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cb7ab-115">-Description</span></span>
<span data-ttu-id="cb7ab-116">Sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="cb7ab-117">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="cb7ab-117">-Exportable</span></span>
<span data-ttu-id="cb7ab-118">Sertifikanın dışarı aktarılaabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7ab-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb7ab-119">-Name</span></span>
<span data-ttu-id="cb7ab-120">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="cb7ab-121">-Parola</span><span class="sxs-lookup"><span data-stu-id="cb7ab-121">-Password</span></span>
<span data-ttu-id="cb7ab-122">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-122">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="cb7ab-123">-Yol</span><span class="sxs-lookup"><span data-stu-id="cb7ab-123">-Path</span></span>
<span data-ttu-id="cb7ab-124">Karşıya yüklenecek bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="cb7ab-125">Dosya. cer veya. pfx olabilir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="cb7ab-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb7ab-126">-Profile</span></span>
<span data-ttu-id="cb7ab-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb7ab-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb7ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7ab-129">CommonParameters</span></span>
<span data-ttu-id="cb7ab-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb7ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7ab-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7ab-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7ab-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb7ab-132">INPUTS</span></span>

## <span data-ttu-id="cb7ab-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb7ab-133">OUTPUTS</span></span>

### <span data-ttu-id="cb7ab-134">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="cb7ab-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="cb7ab-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb7ab-135">NOTES</span></span>

## <span data-ttu-id="cb7ab-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb7ab-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb7ab-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7ab-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="cb7ab-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7ab-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="cb7ab-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7ab-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


