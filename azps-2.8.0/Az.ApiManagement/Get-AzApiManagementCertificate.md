---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 65e9d6783be4814ef4666cfb4dc6405b5004f07e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753595"
---
# <span data-ttu-id="97a4b-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="97a4b-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="97a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="97a4b-103">Hizmette arka uç ile karşılıklı kimlik doğrulama için yapılandırılmış API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="97a4b-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="97a4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97a4b-104">SYNTAX</span></span>

### <span data-ttu-id="97a4b-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97a4b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a4b-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="97a4b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a4b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97a4b-107">DESCRIPTION</span></span>
<span data-ttu-id="97a4b-108">**Get-Azapsananagementcertificate** cmdlet 'i belirttiğiniz tüm Azure API yönetim sertifikalarını veya sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="97a4b-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="97a4b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97a4b-109">EXAMPLES</span></span>

### <span data-ttu-id="97a4b-110">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="97a4b-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="97a4b-111">Bu komut tüm API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="97a4b-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="97a4b-112">Örnek 2: KIMLIĞI olan bir sertifikayı alma</span><span class="sxs-lookup"><span data-stu-id="97a4b-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="97a4b-113">Bu komut belirtilen KIMLIĞE sahip API yönetim sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="97a4b-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="97a4b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="97a4b-115">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="97a4b-115">-CertificateId</span></span>
<span data-ttu-id="97a4b-116">Alınacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="97a4b-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="97a4b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="97a4b-117">-Context</span></span>
<span data-ttu-id="97a4b-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97a4b-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97a4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a4b-119">-DefaultProfile</span></span>
<span data-ttu-id="97a4b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97a4b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a4b-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97a4b-121">-ResourceId</span></span>
<span data-ttu-id="97a4b-122">Sertifikanın ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="97a4b-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="97a4b-123">Belirtilmişse tanımlayıcı tarafından sertifikayı bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="97a4b-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="97a4b-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97a4b-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a4b-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="97a4b-125">-Confirm</span></span>
<span data-ttu-id="97a4b-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97a4b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a4b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a4b-127">-WhatIf</span></span>
<span data-ttu-id="97a4b-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97a4b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a4b-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97a4b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a4b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a4b-130">CommonParameters</span></span>
<span data-ttu-id="97a4b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97a4b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a4b-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97a4b-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a4b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97a4b-133">INPUTS</span></span>

### <span data-ttu-id="97a4b-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="97a4b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97a4b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="97a4b-135">System.String</span></span>

## <span data-ttu-id="97a4b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97a4b-136">OUTPUTS</span></span>

### <span data-ttu-id="97a4b-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="97a4b-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="97a4b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97a4b-138">NOTES</span></span>

## <span data-ttu-id="97a4b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97a4b-139">RELATED LINKS</span></span>

[<span data-ttu-id="97a4b-140">Yeni-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="97a4b-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="97a4b-141">Remove-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="97a4b-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="97a4b-142">Set-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="97a4b-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


