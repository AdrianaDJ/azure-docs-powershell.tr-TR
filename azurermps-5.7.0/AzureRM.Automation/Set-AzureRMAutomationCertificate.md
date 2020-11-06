---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: a1858419b20bf85a40f94e2b5016b461cd24c39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592979"
---
# <span data-ttu-id="a8c04-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8c04-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="a8c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8c04-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c04-103">Otomasyon sertifikasının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8c04-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8c04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8c04-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c04-106">**Set-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda bir sertifikanın yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="a8c04-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8c04-107">EXAMPLES</span></span>

### <span data-ttu-id="a8c04-108">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="a8c04-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a8c04-109">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="a8c04-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="a8c04-110">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a8c04-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="a8c04-111">İkinci komut, Contososertifikası adlı sertifikayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="a8c04-112">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="a8c04-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="a8c04-113">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="a8c04-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8c04-114">PARAMETERS</span></span>

### <span data-ttu-id="a8c04-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8c04-115">-AutomationAccountName</span></span>
<span data-ttu-id="a8c04-116">Bu cmdlet 'in sertifikayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="a8c04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c04-117">-DefaultProfile</span></span>
<span data-ttu-id="a8c04-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a8c04-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8c04-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a8c04-119">-Description</span></span>
<span data-ttu-id="a8c04-120">Bu cmdlet 'in değiştirdiği sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a8c04-121">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="a8c04-121">-Exportable</span></span>
<span data-ttu-id="a8c04-122">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="a8c04-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8c04-123">-Name</span></span>
<span data-ttu-id="a8c04-124">Bu cmdlet 'in değiştirdiği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a8c04-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="a8c04-125">-Password</span></span>
<span data-ttu-id="a8c04-126">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="a8c04-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="a8c04-127">-Path</span></span>
<span data-ttu-id="a8c04-128">Karşıya yüklenecek bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="a8c04-129">Dosya. cer dosyası veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="a8c04-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c04-130">-ResourceGroupName</span></span>
<span data-ttu-id="a8c04-131">Bu cmdlet 'in sertifikayı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8c04-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="a8c04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c04-132">CommonParameters</span></span>
<span data-ttu-id="a8c04-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8c04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c04-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c04-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c04-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8c04-135">INPUTS</span></span>

### <span data-ttu-id="a8c04-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a8c04-136">None</span></span>
<span data-ttu-id="a8c04-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a8c04-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8c04-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8c04-138">OUTPUTS</span></span>

### <span data-ttu-id="a8c04-139">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="a8c04-139">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="a8c04-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8c04-140">NOTES</span></span>

## <span data-ttu-id="a8c04-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8c04-141">RELATED LINKS</span></span>

[<span data-ttu-id="a8c04-142">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8c04-142">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="a8c04-143">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8c04-143">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="a8c04-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8c04-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


