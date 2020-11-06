---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591258"
---
# <span data-ttu-id="52489-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="52489-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="52489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52489-102">SYNOPSIS</span></span>
<span data-ttu-id="52489-103">API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="52489-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52489-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52489-104">SYNTAX</span></span>

### <span data-ttu-id="52489-105">Tüm sertifikaları al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52489-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52489-106">Sertifikayı KIMLIKLE al</span><span class="sxs-lookup"><span data-stu-id="52489-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52489-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52489-107">DESCRIPTION</span></span>
<span data-ttu-id="52489-108">**Get-Azurermapsananagementcertificate** cmdlet 'i belirttiğiniz tüm Azure API yönetim sertifikalarını veya sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="52489-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="52489-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52489-109">EXAMPLES</span></span>

### <span data-ttu-id="52489-110">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="52489-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="52489-111">Bu komut tüm API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="52489-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="52489-112">Örnek 2: KIMLIĞI olan bir sertifikayı alma</span><span class="sxs-lookup"><span data-stu-id="52489-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="52489-113">Bu komut belirtilen KIMLIĞE sahip API yönetim sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="52489-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="52489-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52489-114">PARAMETERS</span></span>

### <span data-ttu-id="52489-115">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="52489-115">-CertificateId</span></span>
<span data-ttu-id="52489-116">Alınacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52489-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52489-117">-Context</span><span class="sxs-lookup"><span data-stu-id="52489-117">-Context</span></span>
<span data-ttu-id="52489-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52489-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="52489-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="52489-119">-Confirm</span></span>
<span data-ttu-id="52489-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52489-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52489-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52489-121">-WhatIf</span></span>
<span data-ttu-id="52489-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52489-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52489-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52489-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52489-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52489-124">-DefaultProfile</span></span>
<span data-ttu-id="52489-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52489-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52489-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52489-126">CommonParameters</span></span>
<span data-ttu-id="52489-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52489-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52489-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52489-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52489-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52489-129">INPUTS</span></span>

## <span data-ttu-id="52489-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52489-130">OUTPUTS</span></span>

### <span data-ttu-id="52489-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="52489-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="52489-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52489-132">NOTES</span></span>

## <span data-ttu-id="52489-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52489-133">RELATED LINKS</span></span>

[<span data-ttu-id="52489-134">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="52489-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="52489-135">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="52489-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="52489-136">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="52489-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


