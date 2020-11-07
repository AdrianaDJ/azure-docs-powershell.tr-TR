---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: cc990e074274917e13b3659aaf0c88f2185f4bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917792"
---
# <span data-ttu-id="1ed6b-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1ed6b-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1ed6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed6b-103">Yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-103">Removes an authorization server.</span></span>

## <span data-ttu-id="1ed6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ed6b-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed6b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ed6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed6b-106">**Remove-Azapsananagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="1ed6b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ed6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed6b-108">Örnek 1: yetkilendirme sunucusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ed6b-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="1ed6b-109">Bu komut belirtilen API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="1ed6b-110">*Force* parametresi belirtildiğinden, hiçbir onay gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="1ed6b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ed6b-111">PARAMETERS</span></span>

### <span data-ttu-id="1ed6b-112">-Context</span><span class="sxs-lookup"><span data-stu-id="1ed6b-112">-Context</span></span>
<span data-ttu-id="1ed6b-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1ed6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed6b-114">-DefaultProfile</span></span>
<span data-ttu-id="1ed6b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed6b-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1ed6b-116">-PassThru</span></span>
<span data-ttu-id="1ed6b-117">geçiş</span><span class="sxs-lookup"><span data-stu-id="1ed6b-117">passthru</span></span>

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

### <span data-ttu-id="1ed6b-118">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="1ed6b-118">-ServerId</span></span>
<span data-ttu-id="1ed6b-119">Kaldırılacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="1ed6b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ed6b-120">-Confirm</span></span>
<span data-ttu-id="1ed6b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed6b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed6b-122">-WhatIf</span></span>
<span data-ttu-id="1ed6b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed6b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed6b-125">CommonParameters</span></span>
<span data-ttu-id="1ed6b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ed6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed6b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed6b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed6b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ed6b-128">INPUTS</span></span>

### <span data-ttu-id="1ed6b-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1ed6b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1ed6b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1ed6b-130">System.String</span></span>

### <span data-ttu-id="1ed6b-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ed6b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ed6b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ed6b-132">OUTPUTS</span></span>

### <span data-ttu-id="1ed6b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ed6b-133">System.Boolean</span></span>

## <span data-ttu-id="1ed6b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ed6b-134">NOTES</span></span>

## <span data-ttu-id="1ed6b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ed6b-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ed6b-136">Get-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="1ed6b-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1ed6b-137">Yeni-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="1ed6b-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1ed6b-138">Set-Azapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="1ed6b-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


