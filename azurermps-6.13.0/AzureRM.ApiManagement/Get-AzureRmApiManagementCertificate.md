---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: af187553ef8ea432299197cd06baefd585e73cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591474"
---
# <span data-ttu-id="bfbc3-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bfbc3-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="bfbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbc3-103">Hizmette arka uç ile karşılıklı kimlik doğrulama için yapılandırılmış API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfbc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfbc3-104">SYNTAX</span></span>

### <span data-ttu-id="bfbc3-105">GetAllCertificates (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bfbc3-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbc3-106">Getbycertificateıd</span><span class="sxs-lookup"><span data-stu-id="bfbc3-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfbc3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfbc3-107">DESCRIPTION</span></span>
<span data-ttu-id="bfbc3-108">**Get-Azurermapsananagementcertificate** cmdlet 'i belirttiğiniz tüm Azure API yönetim sertifikalarını veya sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="bfbc3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfbc3-109">EXAMPLES</span></span>

### <span data-ttu-id="bfbc3-110">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="bfbc3-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="bfbc3-111">Bu komut tüm API yönetim sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="bfbc3-112">Örnek 2: KIMLIĞI olan bir sertifikayı alma</span><span class="sxs-lookup"><span data-stu-id="bfbc3-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="bfbc3-113">Bu komut belirtilen KIMLIĞE sahip API yönetim sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="bfbc3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfbc3-114">PARAMETERS</span></span>

### <span data-ttu-id="bfbc3-115">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="bfbc3-115">-CertificateId</span></span>
<span data-ttu-id="bfbc3-116">Alınacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="bfbc3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bfbc3-117">-Context</span></span>
<span data-ttu-id="bfbc3-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bfbc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbc3-119">-DefaultProfile</span></span>
<span data-ttu-id="bfbc3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfbc3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfbc3-121">-Confirm</span></span>
<span data-ttu-id="bfbc3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbc3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbc3-123">-WhatIf</span></span>
<span data-ttu-id="bfbc3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfbc3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbc3-126">CommonParameters</span></span>
<span data-ttu-id="bfbc3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfbc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbc3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfbc3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbc3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfbc3-129">INPUTS</span></span>

### <span data-ttu-id="bfbc3-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="bfbc3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bfbc3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbc3-131">System.String</span></span>

## <span data-ttu-id="bfbc3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfbc3-132">OUTPUTS</span></span>

### <span data-ttu-id="bfbc3-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="bfbc3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="bfbc3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfbc3-134">NOTES</span></span>

## <span data-ttu-id="bfbc3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfbc3-135">RELATED LINKS</span></span>

[<span data-ttu-id="bfbc3-136">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="bfbc3-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="bfbc3-137">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="bfbc3-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="bfbc3-138">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="bfbc3-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


