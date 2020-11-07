---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937402"
---
# <span data-ttu-id="c6a8e-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6a8e-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="c6a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a8e-103">Otomasyon sertifikasının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="c6a8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6a8e-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a8e-106">**Set-AzAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda bir sertifikanın yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="c6a8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a8e-108">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="c6a8e-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c6a8e-109">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c6a8e-110">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="c6a8e-111">İkinci komut, Contososertifikası adlı sertifikayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="c6a8e-112">Komut $Password uygulamasında depolanan parolayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="c6a8e-113">Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="c6a8e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6a8e-114">PARAMETERS</span></span>

### <span data-ttu-id="c6a8e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6a8e-115">-AutomationAccountName</span></span>
<span data-ttu-id="c6a8e-116">Bu cmdlet 'in sertifikayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="c6a8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a8e-117">-DefaultProfile</span></span>
<span data-ttu-id="c6a8e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c6a8e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6a8e-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c6a8e-119">-Description</span></span>
<span data-ttu-id="c6a8e-120">Bu cmdlet 'in değiştirdiği sertifikanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c6a8e-121">-Dışarı aktarılabilir</span><span class="sxs-lookup"><span data-stu-id="c6a8e-121">-Exportable</span></span>
<span data-ttu-id="c6a8e-122">Sertifikanın dışarı aktarılabildiğinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="c6a8e-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6a8e-123">-Name</span></span>
<span data-ttu-id="c6a8e-124">Bu cmdlet 'in değiştirdiği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c6a8e-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="c6a8e-125">-Password</span></span>
<span data-ttu-id="c6a8e-126">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="c6a8e-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="c6a8e-127">-Path</span></span>
<span data-ttu-id="c6a8e-128">Karşıya yüklenecek bir komut dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="c6a8e-129">Dosya. cer dosyası veya. pfx dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="c6a8e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a8e-130">-ResourceGroupName</span></span>
<span data-ttu-id="c6a8e-131">Bu cmdlet 'in sertifikayı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="c6a8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a8e-132">CommonParameters</span></span>
<span data-ttu-id="c6a8e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6a8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a8e-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a8e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a8e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6a8e-135">INPUTS</span></span>

### <span data-ttu-id="c6a8e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c6a8e-136">System.String</span></span>

### <span data-ttu-id="c6a8e-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c6a8e-137">System.Security.SecureString</span></span>

### <span data-ttu-id="c6a8e-138">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6a8e-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c6a8e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6a8e-139">OUTPUTS</span></span>

### <span data-ttu-id="c6a8e-140">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="c6a8e-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="c6a8e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6a8e-141">NOTES</span></span>

## <span data-ttu-id="c6a8e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6a8e-142">RELATED LINKS</span></span>

[<span data-ttu-id="c6a8e-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6a8e-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="c6a8e-144">Yeni-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6a8e-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="c6a8e-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6a8e-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


