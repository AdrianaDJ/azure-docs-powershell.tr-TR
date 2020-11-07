---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 52d40ed69adda157a8fdacd9d6c961f88508fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751164"
---
# <span data-ttu-id="06545-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="06545-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="06545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06545-102">SYNOPSIS</span></span>
<span data-ttu-id="06545-103">Hizmette arka uç ile karşılıklı kimlik doğrulama için yapılandırılmış API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="06545-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="06545-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06545-104">SYNTAX</span></span>

### <span data-ttu-id="06545-105">GetAllCertificates (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06545-105">GetAllCertificates (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06545-106">Getbycertificateıd</span><span class="sxs-lookup"><span data-stu-id="06545-106">GetByCertificateId</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06545-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="06545-107">DESCRIPTION</span></span>
<span data-ttu-id="06545-108">**Get-Azapsananagementcertificate** cmdlet 'i belirttiğiniz tüm Azure API yönetim sertifikalarını veya sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="06545-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="06545-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06545-109">EXAMPLES</span></span>

### <span data-ttu-id="06545-110">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="06545-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="06545-111">Bu komut tüm API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="06545-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="06545-112">Örnek 2: KIMLIĞI olan bir sertifikayı alma</span><span class="sxs-lookup"><span data-stu-id="06545-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="06545-113">Bu komut belirtilen KIMLIĞE sahip API yönetim sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="06545-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="06545-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06545-114">PARAMETERS</span></span>

### <span data-ttu-id="06545-115">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="06545-115">-CertificateId</span></span>
<span data-ttu-id="06545-116">Alınacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06545-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06545-117">-Context</span><span class="sxs-lookup"><span data-stu-id="06545-117">-Context</span></span>
<span data-ttu-id="06545-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06545-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06545-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06545-119">-DefaultProfile</span></span>
<span data-ttu-id="06545-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06545-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06545-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="06545-121">-Confirm</span></span>
<span data-ttu-id="06545-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06545-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06545-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06545-123">-WhatIf</span></span>
<span data-ttu-id="06545-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06545-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06545-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06545-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06545-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06545-126">CommonParameters</span></span>
<span data-ttu-id="06545-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06545-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06545-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06545-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06545-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06545-129">INPUTS</span></span>

### <span data-ttu-id="06545-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="06545-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="06545-131">System. String</span><span class="sxs-lookup"><span data-stu-id="06545-131">System.String</span></span>

## <span data-ttu-id="06545-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06545-132">OUTPUTS</span></span>

### <span data-ttu-id="06545-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="06545-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="06545-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06545-134">NOTES</span></span>

## <span data-ttu-id="06545-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06545-135">RELATED LINKS</span></span>

[<span data-ttu-id="06545-136">Yeni-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="06545-136">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="06545-137">Remove-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="06545-137">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="06545-138">Set-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="06545-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


