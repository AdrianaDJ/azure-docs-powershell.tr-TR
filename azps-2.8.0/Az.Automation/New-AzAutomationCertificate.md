---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 1c3c3cb4fecfde01926e21a75470fc945f8c86c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753281"
---
# <span data-ttu-id="60108-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60108-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="60108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60108-102">SYNOPSIS</span></span>
<span data-ttu-id="60108-103">Otomasyon sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60108-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="60108-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60108-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60108-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60108-105">DESCRIPTION</span></span>
<span data-ttu-id="60108-106">**Yeni-AzAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60108-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="60108-107">Karşıya yüklenecek sertifika dosyasının yolunu sağlayın.</span><span class="sxs-lookup"><span data-stu-id="60108-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="60108-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60108-108">EXAMPLES</span></span>

### <span data-ttu-id="60108-109">Örnek 1: yeni sertifika oluşturma</span><span class="sxs-lookup"><span data-stu-id="60108-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60108-110">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="60108-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="60108-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="60108-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="60108-112">İkinci komut, ContosoCertificate adlı bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60108-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="60108-113">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="60108-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="60108-114">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="60108-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60108-115">PARAMETERS</span></span>

### <span data-ttu-id="60108-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60108-116">-AutomationAccountName</span></span>
<span data-ttu-id="60108-117">Bu cmdlet 'in sertifikayı sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="60108-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60108-118">-DefaultProfile</span></span>
<span data-ttu-id="60108-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="60108-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60108-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="60108-120">-Description</span></span>
<span data-ttu-id="60108-121">Sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="60108-122">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="60108-122">-Exportable</span></span>
<span data-ttu-id="60108-123">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="60108-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="60108-124">-Name</span></span>
<span data-ttu-id="60108-125">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="60108-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="60108-126">-Password</span></span>
<span data-ttu-id="60108-127">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="60108-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="60108-128">-Path</span></span>
<span data-ttu-id="60108-129">Bu cmdlet 'in karşıya yüklemelerinin bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="60108-130">Dosya bir. cer veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="60108-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="60108-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60108-131">-ResourceGroupName</span></span>
<span data-ttu-id="60108-132">Bu cmdlet 'in sertifika oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60108-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="60108-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60108-133">CommonParameters</span></span>
<span data-ttu-id="60108-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60108-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60108-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60108-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60108-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60108-136">INPUTS</span></span>

### <span data-ttu-id="60108-137">System. String</span><span class="sxs-lookup"><span data-stu-id="60108-137">System.String</span></span>

### <span data-ttu-id="60108-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="60108-138">System.Security.SecureString</span></span>

### <span data-ttu-id="60108-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60108-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60108-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60108-140">OUTPUTS</span></span>

### <span data-ttu-id="60108-141">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="60108-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="60108-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60108-142">NOTES</span></span>

<span data-ttu-id="60108-143">Bu komut, yönetici olduğunuz bir makinede, ayrıca yükseltilmiş bir PowerShell oturumunda çalıştırılmalıdır; Sertifika yüklenmeden önce, bu cmdlet yerel X. 509.440 deposunu kullanarak parmak izi ve anahtarı alır ve bu cmdlet yükseltilmiş PowerShell oturumu dışında çalıştırıldığında, "erişim reddedildi" hatası alırsınız.</span><span class="sxs-lookup"><span data-stu-id="60108-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="60108-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60108-144">RELATED LINKS</span></span>

[<span data-ttu-id="60108-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60108-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="60108-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60108-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="60108-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60108-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


