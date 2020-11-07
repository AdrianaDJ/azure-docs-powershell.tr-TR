---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 1eab0b6f9f80a4fb921a64966c758cdaa08c51df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753420"
---
# <span data-ttu-id="88db5-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="88db5-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="88db5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88db5-102">SYNOPSIS</span></span>
<span data-ttu-id="88db5-103">Arka uç ile karşılıklı kimlik doğrulama için yapılandırılmış bir API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88db5-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="88db5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88db5-104">SYNTAX</span></span>

### <span data-ttu-id="88db5-105">LoadFromFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88db5-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88db5-106">Ham</span><span class="sxs-lookup"><span data-stu-id="88db5-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88db5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88db5-107">DESCRIPTION</span></span>
<span data-ttu-id="88db5-108">**Set-Azapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88db5-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="88db5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88db5-109">EXAMPLES</span></span>

### <span data-ttu-id="88db5-110">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="88db5-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="88db5-111">Bu komut belirtilen API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88db5-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="88db5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88db5-112">PARAMETERS</span></span>

### <span data-ttu-id="88db5-113">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="88db5-113">-CertificateId</span></span>
<span data-ttu-id="88db5-114">Değiştirilecek sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="88db5-114">Specifies the ID of the certificate to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88db5-115">-Context</span><span class="sxs-lookup"><span data-stu-id="88db5-115">-Context</span></span>
<span data-ttu-id="88db5-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88db5-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88db5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88db5-117">-DefaultProfile</span></span>
<span data-ttu-id="88db5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88db5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88db5-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="88db5-119">-PassThru</span></span>
<span data-ttu-id="88db5-120">geçiş</span><span class="sxs-lookup"><span data-stu-id="88db5-120">passthru</span></span>

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

### <span data-ttu-id="88db5-121">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="88db5-121">-PfxBytes</span></span>
<span data-ttu-id="88db5-122">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88db5-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="88db5-123">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="88db5-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88db5-124">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="88db5-124">-PfxFilePath</span></span>
<span data-ttu-id="88db5-125">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="88db5-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="88db5-126">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="88db5-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88db5-127">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="88db5-127">-PfxPassword</span></span>
<span data-ttu-id="88db5-128">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88db5-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88db5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88db5-129">CommonParameters</span></span>
<span data-ttu-id="88db5-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88db5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88db5-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88db5-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88db5-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88db5-132">INPUTS</span></span>

### <span data-ttu-id="88db5-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="88db5-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="88db5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="88db5-134">System.String</span></span>

### <span data-ttu-id="88db5-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="88db5-135">System.Byte[]</span></span>

### <span data-ttu-id="88db5-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88db5-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88db5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88db5-137">OUTPUTS</span></span>

### <span data-ttu-id="88db5-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="88db5-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="88db5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88db5-139">NOTES</span></span>

## <span data-ttu-id="88db5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88db5-140">RELATED LINKS</span></span>

[<span data-ttu-id="88db5-141">Get-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="88db5-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="88db5-142">Yeni-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="88db5-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="88db5-143">Remove-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="88db5-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


