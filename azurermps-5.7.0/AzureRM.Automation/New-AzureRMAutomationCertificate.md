---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586824"
---
# <span data-ttu-id="1b63d-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b63d-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="1b63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b63d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b63d-103">Otomasyon sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b63d-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b63d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b63d-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b63d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b63d-105">DESCRIPTION</span></span>
<span data-ttu-id="1b63d-106">**Yeni-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b63d-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="1b63d-107">Karşıya yüklenecek sertifika dosyasının yolunu sağlayın.</span><span class="sxs-lookup"><span data-stu-id="1b63d-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="1b63d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b63d-108">EXAMPLES</span></span>

### <span data-ttu-id="1b63d-109">Örnek 1: yeni sertifika oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b63d-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1b63d-110">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="1b63d-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="1b63d-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1b63d-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="1b63d-112">İkinci komut, ContosoCertificate adlı bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b63d-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="1b63d-113">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="1b63d-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="1b63d-114">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="1b63d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b63d-115">PARAMETERS</span></span>

### <span data-ttu-id="1b63d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1b63d-116">-AutomationAccountName</span></span>
<span data-ttu-id="1b63d-117">Bu cmdlet 'in sertifikayı sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="1b63d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b63d-118">-DefaultProfile</span></span>
<span data-ttu-id="1b63d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1b63d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b63d-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1b63d-120">-Description</span></span>
<span data-ttu-id="1b63d-121">Sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="1b63d-122">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="1b63d-122">-Exportable</span></span>
<span data-ttu-id="1b63d-123">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="1b63d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b63d-124">-Name</span></span>
<span data-ttu-id="1b63d-125">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="1b63d-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="1b63d-126">-Password</span></span>
<span data-ttu-id="1b63d-127">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="1b63d-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="1b63d-128">-Path</span></span>
<span data-ttu-id="1b63d-129">Bu cmdlet 'in karşıya yüklemelerinin bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="1b63d-130">Dosya bir. cer veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="1b63d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b63d-131">-ResourceGroupName</span></span>
<span data-ttu-id="1b63d-132">Bu cmdlet 'in sertifika oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b63d-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="1b63d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b63d-133">CommonParameters</span></span>
<span data-ttu-id="1b63d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b63d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b63d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b63d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b63d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b63d-136">INPUTS</span></span>

### <span data-ttu-id="1b63d-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b63d-137">None</span></span>
<span data-ttu-id="1b63d-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1b63d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b63d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b63d-139">OUTPUTS</span></span>

### <span data-ttu-id="1b63d-140">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="1b63d-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1b63d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b63d-141">NOTES</span></span>

## <span data-ttu-id="1b63d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b63d-142">RELATED LINKS</span></span>

[<span data-ttu-id="1b63d-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b63d-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1b63d-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b63d-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1b63d-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b63d-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


