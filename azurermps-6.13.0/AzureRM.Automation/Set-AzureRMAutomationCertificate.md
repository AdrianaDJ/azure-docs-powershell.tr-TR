---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 549bc5bb67eab5287bf463f7e816cc0ff597cf52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588610"
---
# <span data-ttu-id="97e40-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="97e40-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="97e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e40-102">SYNOPSIS</span></span>
<span data-ttu-id="97e40-103">Otomasyon sertifikasının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="97e40-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97e40-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97e40-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97e40-105">DESCRIPTION</span></span>
<span data-ttu-id="97e40-106">**Set-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda bir sertifikanın yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="97e40-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="97e40-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97e40-107">EXAMPLES</span></span>

### <span data-ttu-id="97e40-108">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="97e40-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="97e40-109">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="97e40-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="97e40-110">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="97e40-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="97e40-111">İkinci komut, Contososertifikası adlı sertifikayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="97e40-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="97e40-112">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="97e40-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="97e40-113">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="97e40-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97e40-114">PARAMETERS</span></span>

### <span data-ttu-id="97e40-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97e40-115">-AutomationAccountName</span></span>
<span data-ttu-id="97e40-116">Bu cmdlet 'in sertifikayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="97e40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e40-117">-DefaultProfile</span></span>
<span data-ttu-id="97e40-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97e40-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97e40-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="97e40-119">-Description</span></span>
<span data-ttu-id="97e40-120">Bu cmdlet 'in değiştirdiği sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="97e40-121">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="97e40-121">-Exportable</span></span>
<span data-ttu-id="97e40-122">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="97e40-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="97e40-123">-Name</span></span>
<span data-ttu-id="97e40-124">Bu cmdlet 'in değiştirdiği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="97e40-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="97e40-125">-Password</span></span>
<span data-ttu-id="97e40-126">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="97e40-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="97e40-127">-Path</span></span>
<span data-ttu-id="97e40-128">Karşıya yüklenecek bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="97e40-129">Dosya. cer dosyası veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="97e40-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="97e40-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e40-130">-ResourceGroupName</span></span>
<span data-ttu-id="97e40-131">Bu cmdlet 'in sertifikayı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e40-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="97e40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e40-132">CommonParameters</span></span>
<span data-ttu-id="97e40-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97e40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e40-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e40-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97e40-135">INPUTS</span></span>

### <span data-ttu-id="97e40-136">System. String</span><span class="sxs-lookup"><span data-stu-id="97e40-136">System.String</span></span>

### <span data-ttu-id="97e40-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="97e40-137">System.Security.SecureString</span></span>

### <span data-ttu-id="97e40-138">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="97e40-138">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="97e40-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97e40-139">OUTPUTS</span></span>

### <span data-ttu-id="97e40-140">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="97e40-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="97e40-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97e40-141">NOTES</span></span>

## <span data-ttu-id="97e40-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97e40-142">RELATED LINKS</span></span>

[<span data-ttu-id="97e40-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="97e40-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="97e40-144">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="97e40-144">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="97e40-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="97e40-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


