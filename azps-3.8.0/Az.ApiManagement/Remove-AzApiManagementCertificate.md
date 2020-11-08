---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097705"
---
# <span data-ttu-id="8b06c-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8b06c-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="8b06c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b06c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b06c-103">Bir API yönetim sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b06c-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="8b06c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b06c-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b06c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b06c-105">DESCRIPTION</span></span>
<span data-ttu-id="8b06c-106">**Remove-Azapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b06c-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="8b06c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b06c-107">EXAMPLES</span></span>

### <span data-ttu-id="8b06c-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b06c-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="8b06c-109">Bu komut belirtilen API yönetim sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b06c-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="8b06c-110">*Force* parametresi belirtildiğinden, hiçbir onay gerekmez.</span><span class="sxs-lookup"><span data-stu-id="8b06c-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="8b06c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b06c-111">PARAMETERS</span></span>

### <span data-ttu-id="8b06c-112">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="8b06c-112">-CertificateId</span></span>
<span data-ttu-id="8b06c-113">Kaldırılacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b06c-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="8b06c-114">-Context</span><span class="sxs-lookup"><span data-stu-id="8b06c-114">-Context</span></span>
<span data-ttu-id="8b06c-115">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b06c-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8b06c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b06c-116">-DefaultProfile</span></span>
<span data-ttu-id="8b06c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b06c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b06c-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8b06c-118">-PassThru</span></span>
<span data-ttu-id="8b06c-119">geçiş</span><span class="sxs-lookup"><span data-stu-id="8b06c-119">passthru</span></span>

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

### <span data-ttu-id="8b06c-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b06c-120">-Confirm</span></span>
<span data-ttu-id="8b06c-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b06c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b06c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b06c-122">-WhatIf</span></span>
<span data-ttu-id="8b06c-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b06c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b06c-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b06c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b06c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b06c-125">CommonParameters</span></span>
<span data-ttu-id="8b06c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b06c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b06c-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8b06c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b06c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b06c-128">INPUTS</span></span>

### <span data-ttu-id="8b06c-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8b06c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b06c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8b06c-130">System.String</span></span>

### <span data-ttu-id="8b06c-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b06c-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b06c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b06c-132">OUTPUTS</span></span>

### <span data-ttu-id="8b06c-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b06c-133">System.Boolean</span></span>

## <span data-ttu-id="8b06c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b06c-134">NOTES</span></span>

## <span data-ttu-id="8b06c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b06c-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b06c-136">Get-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="8b06c-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="8b06c-137">Yeni-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="8b06c-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="8b06c-138">Set-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="8b06c-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


