---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109873"
---
# <span data-ttu-id="6d80a-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="6d80a-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="6d80a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d80a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d80a-103">Yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d80a-103">Removes an authorization server.</span></span>

## <span data-ttu-id="6d80a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d80a-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d80a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d80a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d80a-106">**Remove-Azapsananagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d80a-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="6d80a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d80a-107">EXAMPLES</span></span>

### <span data-ttu-id="6d80a-108">Örnek 1: yetkilendirme sunucusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="6d80a-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="6d80a-109">Bu komut belirtilen API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d80a-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="6d80a-110">*Force* parametresi belirtildiğinden, hiçbir onay gerekmez.</span><span class="sxs-lookup"><span data-stu-id="6d80a-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="6d80a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d80a-111">PARAMETERS</span></span>

### <span data-ttu-id="6d80a-112">-Context</span><span class="sxs-lookup"><span data-stu-id="6d80a-112">-Context</span></span>
<span data-ttu-id="6d80a-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d80a-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6d80a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d80a-114">-DefaultProfile</span></span>
<span data-ttu-id="6d80a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d80a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d80a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6d80a-116">-PassThru</span></span>
<span data-ttu-id="6d80a-117">geçiş</span><span class="sxs-lookup"><span data-stu-id="6d80a-117">passthru</span></span>

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

### <span data-ttu-id="6d80a-118">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="6d80a-118">-ServerId</span></span>
<span data-ttu-id="6d80a-119">Kaldırılacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d80a-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="6d80a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d80a-120">-Confirm</span></span>
<span data-ttu-id="6d80a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d80a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d80a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d80a-122">-WhatIf</span></span>
<span data-ttu-id="6d80a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d80a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d80a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d80a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d80a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d80a-125">CommonParameters</span></span>
<span data-ttu-id="6d80a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d80a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d80a-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6d80a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d80a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d80a-128">INPUTS</span></span>

### <span data-ttu-id="6d80a-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6d80a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d80a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6d80a-130">System.String</span></span>

### <span data-ttu-id="6d80a-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d80a-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6d80a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d80a-132">OUTPUTS</span></span>

### <span data-ttu-id="6d80a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d80a-133">System.Boolean</span></span>

## <span data-ttu-id="6d80a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d80a-134">NOTES</span></span>

## <span data-ttu-id="6d80a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d80a-135">RELATED LINKS</span></span>

[<span data-ttu-id="6d80a-136">Get-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="6d80a-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="6d80a-137">Yeni-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="6d80a-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="6d80a-138">Set-Azapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="6d80a-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


