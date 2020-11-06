---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: a3e662d031c036686298beaa5c80bd4efa8a3888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591183"
---
# <span data-ttu-id="ae13e-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae13e-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="ae13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae13e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae13e-103">Otomasyon sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae13e-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae13e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae13e-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae13e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae13e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae13e-106">**Yeni-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae13e-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="ae13e-107">Karşıya yüklenecek sertifika dosyasının yolunu sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ae13e-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="ae13e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae13e-108">EXAMPLES</span></span>

### <span data-ttu-id="ae13e-109">Örnek 1: yeni sertifika oluşturma</span><span class="sxs-lookup"><span data-stu-id="ae13e-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ae13e-110">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="ae13e-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="ae13e-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ae13e-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="ae13e-112">İkinci komut, ContosoCertificate adlı bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae13e-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="ae13e-113">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="ae13e-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="ae13e-114">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="ae13e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae13e-115">PARAMETERS</span></span>

### <span data-ttu-id="ae13e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ae13e-116">-AutomationAccountName</span></span>
<span data-ttu-id="ae13e-117">Bu cmdlet 'in sertifikayı sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13e-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ae13e-118">-Description</span></span>
<span data-ttu-id="ae13e-119">Sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-119">Specifies a description for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13e-120">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="ae13e-120">-Exportable</span></span>
<span data-ttu-id="ae13e-121">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-121">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae13e-122">-Name</span></span>
<span data-ttu-id="ae13e-123">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-123">Specifies the name for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13e-124">-Parola</span><span class="sxs-lookup"><span data-stu-id="ae13e-124">-Password</span></span>
<span data-ttu-id="ae13e-125">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-125">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13e-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="ae13e-126">-Path</span></span>
<span data-ttu-id="ae13e-127">Bu cmdlet 'in karşıya yüklemelerinin bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-127">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="ae13e-128">Dosya bir. cer veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-128">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae13e-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae13e-130">Bu cmdlet 'in sertifika oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13e-130">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ae13e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae13e-131">-DefaultProfile</span></span>
<span data-ttu-id="ae13e-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae13e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae13e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae13e-133">CommonParameters</span></span>
<span data-ttu-id="ae13e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae13e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae13e-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae13e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae13e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae13e-136">INPUTS</span></span>

## <span data-ttu-id="ae13e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae13e-137">OUTPUTS</span></span>

### <span data-ttu-id="ae13e-138">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="ae13e-138">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ae13e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae13e-139">NOTES</span></span>

## <span data-ttu-id="ae13e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae13e-140">RELATED LINKS</span></span>

[<span data-ttu-id="ae13e-141">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae13e-141">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="ae13e-142">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae13e-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="ae13e-143">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae13e-143">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


