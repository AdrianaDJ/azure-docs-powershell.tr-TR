---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: 83ec5c8cd9dd9937ca372441d5a9be005bffc76a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589606"
---
# <span data-ttu-id="2604c-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2604c-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="2604c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2604c-102">SYNOPSIS</span></span>
<span data-ttu-id="2604c-103">Otomasyon sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2604c-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2604c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2604c-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2604c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2604c-105">DESCRIPTION</span></span>
<span data-ttu-id="2604c-106">**Yeni-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2604c-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="2604c-107">Karşıya yüklenecek sertifika dosyasının yolunu sağlayın.</span><span class="sxs-lookup"><span data-stu-id="2604c-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="2604c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2604c-108">EXAMPLES</span></span>

### <span data-ttu-id="2604c-109">Örnek 1: yeni sertifika oluşturma</span><span class="sxs-lookup"><span data-stu-id="2604c-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2604c-110">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="2604c-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="2604c-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2604c-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="2604c-112">İkinci komut, ContosoCertificate adlı bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2604c-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="2604c-113">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="2604c-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="2604c-114">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="2604c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2604c-115">PARAMETERS</span></span>

### <span data-ttu-id="2604c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2604c-116">-AutomationAccountName</span></span>
<span data-ttu-id="2604c-117">Bu cmdlet 'in sertifikayı sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="2604c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2604c-118">-DefaultProfile</span></span>
<span data-ttu-id="2604c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2604c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2604c-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2604c-120">-Description</span></span>
<span data-ttu-id="2604c-121">Sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="2604c-122">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="2604c-122">-Exportable</span></span>
<span data-ttu-id="2604c-123">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="2604c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2604c-124">-Name</span></span>
<span data-ttu-id="2604c-125">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="2604c-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="2604c-126">-Password</span></span>
<span data-ttu-id="2604c-127">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="2604c-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="2604c-128">-Path</span></span>
<span data-ttu-id="2604c-129">Bu cmdlet 'in karşıya yüklemelerinin bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="2604c-130">Dosya bir. cer veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="2604c-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="2604c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2604c-131">-ResourceGroupName</span></span>
<span data-ttu-id="2604c-132">Bu cmdlet 'in sertifika oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2604c-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="2604c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2604c-133">CommonParameters</span></span>
<span data-ttu-id="2604c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2604c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2604c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2604c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2604c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2604c-136">INPUTS</span></span>

### <span data-ttu-id="2604c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2604c-137">System.String</span></span>

### <span data-ttu-id="2604c-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="2604c-138">System.Security.SecureString</span></span>

### <span data-ttu-id="2604c-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2604c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2604c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2604c-140">OUTPUTS</span></span>

### <span data-ttu-id="2604c-141">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="2604c-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="2604c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2604c-142">NOTES</span></span>

## <span data-ttu-id="2604c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2604c-143">RELATED LINKS</span></span>

[<span data-ttu-id="2604c-144">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2604c-144">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="2604c-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2604c-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="2604c-146">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2604c-146">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


