---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 97a5db6a816b2274befde1d4efb898b0c5e2bfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595038"
---
# <span data-ttu-id="bce9b-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bce9b-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="bce9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce9b-102">SYNOPSIS</span></span>
<span data-ttu-id="bce9b-103">Otomasyon sertifikasının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bce9b-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce9b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bce9b-105">DESCRIPTION</span></span>
<span data-ttu-id="bce9b-106">**Set-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda bir sertifikanın yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="bce9b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bce9b-107">EXAMPLES</span></span>

### <span data-ttu-id="bce9b-108">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="bce9b-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bce9b-109">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="bce9b-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="bce9b-110">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bce9b-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="bce9b-111">İkinci komut, Contososertifikası adlı sertifikayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="bce9b-112">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="bce9b-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="bce9b-113">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="bce9b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bce9b-114">PARAMETERS</span></span>

### <span data-ttu-id="bce9b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bce9b-115">-AutomationAccountName</span></span>
<span data-ttu-id="bce9b-116">Bu cmdlet 'in sertifikayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="bce9b-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="bce9b-117">-Description</span></span>
<span data-ttu-id="bce9b-118">Bu cmdlet 'in değiştirdiği sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-118">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bce9b-119">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="bce9b-119">-Exportable</span></span>
<span data-ttu-id="bce9b-120">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-120">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce9b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bce9b-121">-Name</span></span>
<span data-ttu-id="bce9b-122">Bu cmdlet 'in değiştirdiği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-122">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bce9b-123">-Parola</span><span class="sxs-lookup"><span data-stu-id="bce9b-123">-Password</span></span>
<span data-ttu-id="bce9b-124">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-124">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="bce9b-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="bce9b-125">-Path</span></span>
<span data-ttu-id="bce9b-126">Karşıya yüklenecek bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-126">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="bce9b-127">Dosya. cer dosyası veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-127">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="bce9b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce9b-128">-ResourceGroupName</span></span>
<span data-ttu-id="bce9b-129">Bu cmdlet 'in sertifikayı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bce9b-129">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="bce9b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce9b-130">-DefaultProfile</span></span>
<span data-ttu-id="bce9b-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bce9b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bce9b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce9b-132">CommonParameters</span></span>
<span data-ttu-id="bce9b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bce9b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce9b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce9b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce9b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bce9b-135">INPUTS</span></span>

## <span data-ttu-id="bce9b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bce9b-136">OUTPUTS</span></span>

### <span data-ttu-id="bce9b-137">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="bce9b-137">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="bce9b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bce9b-138">NOTES</span></span>

## <span data-ttu-id="bce9b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bce9b-139">RELATED LINKS</span></span>

[<span data-ttu-id="bce9b-140">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bce9b-140">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="bce9b-141">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bce9b-141">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="bce9b-142">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bce9b-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


