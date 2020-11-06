---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573069"
---
# <span data-ttu-id="ccb3b-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ccb3b-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="ccb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb3b-103">Yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccb3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccb3b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccb3b-105">DESCRIPTION</span></span>
<span data-ttu-id="ccb3b-106">**Remove-Azurermapsananagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="ccb3b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccb3b-107">EXAMPLES</span></span>

## <span data-ttu-id="ccb3b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccb3b-108">PARAMETERS</span></span>

### <span data-ttu-id="ccb3b-109">-Context</span><span class="sxs-lookup"><span data-stu-id="ccb3b-109">-Context</span></span>
<span data-ttu-id="ccb3b-110">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ccb3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb3b-111">-DefaultProfile</span></span>
<span data-ttu-id="ccb3b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccb3b-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ccb3b-113">-PassThru</span></span>
<span data-ttu-id="ccb3b-114">geçiş</span><span class="sxs-lookup"><span data-stu-id="ccb3b-114">passthru</span></span>

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

### <span data-ttu-id="ccb3b-115">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="ccb3b-115">-ServerId</span></span>
<span data-ttu-id="ccb3b-116">Kaldırılacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="ccb3b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccb3b-117">-Confirm</span></span>
<span data-ttu-id="ccb3b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb3b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb3b-119">-WhatIf</span></span>
<span data-ttu-id="ccb3b-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccb3b-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb3b-122">CommonParameters</span></span>
<span data-ttu-id="ccb3b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb3b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb3b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccb3b-125">INPUTS</span></span>

### <span data-ttu-id="ccb3b-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ccb3b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ccb3b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ccb3b-127">System.String</span></span>

### <span data-ttu-id="ccb3b-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ccb3b-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ccb3b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccb3b-129">OUTPUTS</span></span>

### <span data-ttu-id="ccb3b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccb3b-130">System.Boolean</span></span>

## <span data-ttu-id="ccb3b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccb3b-131">NOTES</span></span>

## <span data-ttu-id="ccb3b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccb3b-132">RELATED LINKS</span></span>

[<span data-ttu-id="ccb3b-133">Get-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="ccb3b-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="ccb3b-134">Yeni-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="ccb3b-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="ccb3b-135">Set-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="ccb3b-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


