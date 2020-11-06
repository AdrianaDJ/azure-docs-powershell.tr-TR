---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a70e3323bbd154005f014f1064a535f45a102f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573061"
---
# <span data-ttu-id="6c5fd-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5fd-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="6c5fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5fd-103">Bir API yönetim sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c5fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c5fd-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c5fd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c5fd-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5fd-106">**Remove-Azurermapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="6c5fd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c5fd-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5fd-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="6c5fd-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="6c5fd-109">Bu komut belirtilen API yönetim sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="6c5fd-110">*Force* parametresi belirtildiğinden, hiçbir onay gerekmez.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="6c5fd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c5fd-111">PARAMETERS</span></span>

### <span data-ttu-id="6c5fd-112">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="6c5fd-112">-CertificateId</span></span>
<span data-ttu-id="6c5fd-113">Kaldırılacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="6c5fd-114">-Context</span><span class="sxs-lookup"><span data-stu-id="6c5fd-114">-Context</span></span>
<span data-ttu-id="6c5fd-115">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6c5fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5fd-116">-DefaultProfile</span></span>
<span data-ttu-id="6c5fd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c5fd-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6c5fd-118">-PassThru</span></span>
<span data-ttu-id="6c5fd-119">geçiş</span><span class="sxs-lookup"><span data-stu-id="6c5fd-119">passthru</span></span>

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

### <span data-ttu-id="6c5fd-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c5fd-120">-Confirm</span></span>
<span data-ttu-id="6c5fd-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c5fd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c5fd-122">-WhatIf</span></span>
<span data-ttu-id="6c5fd-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c5fd-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c5fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5fd-125">CommonParameters</span></span>
<span data-ttu-id="6c5fd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5fd-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5fd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5fd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c5fd-128">INPUTS</span></span>

### <span data-ttu-id="6c5fd-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6c5fd-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6c5fd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6c5fd-130">System.String</span></span>

### <span data-ttu-id="6c5fd-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6c5fd-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6c5fd-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c5fd-132">OUTPUTS</span></span>

### <span data-ttu-id="6c5fd-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c5fd-133">System.Boolean</span></span>

## <span data-ttu-id="6c5fd-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c5fd-134">NOTES</span></span>

## <span data-ttu-id="6c5fd-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c5fd-135">RELATED LINKS</span></span>

[<span data-ttu-id="6c5fd-136">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="6c5fd-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="6c5fd-137">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="6c5fd-137">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="6c5fd-138">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="6c5fd-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


