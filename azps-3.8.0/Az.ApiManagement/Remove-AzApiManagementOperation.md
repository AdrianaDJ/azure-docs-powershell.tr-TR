---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097629"
---
# <span data-ttu-id="57c3b-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="57c3b-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="57c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="57c3b-103">Var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57c3b-103">Removes an existing operation.</span></span>

## <span data-ttu-id="57c3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57c3b-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57c3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="57c3b-106">**Remove-Azapsananagementoperation** cmdlet 'i var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57c3b-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="57c3b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="57c3b-108">Örnek 1: var olan bir API Işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="57c3b-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="57c3b-109">Bu komut, var olan bir API Işlemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57c3b-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="57c3b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57c3b-110">PARAMETERS</span></span>

### <span data-ttu-id="57c3b-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="57c3b-111">-ApiId</span></span>
<span data-ttu-id="57c3b-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57c3b-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="57c3b-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="57c3b-113">-ApiRevision</span></span>
<span data-ttu-id="57c3b-114">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="57c3b-114">Identifier of API Revision.</span></span> <span data-ttu-id="57c3b-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="57c3b-115">This parameter is optional.</span></span> <span data-ttu-id="57c3b-116">Belirtilmezse, işlem geçerli API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="57c3b-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="57c3b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="57c3b-117">-Context</span></span>
<span data-ttu-id="57c3b-118">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57c3b-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="57c3b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c3b-119">-DefaultProfile</span></span>
<span data-ttu-id="57c3b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57c3b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57c3b-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="57c3b-121">-OperationId</span></span>
<span data-ttu-id="57c3b-122">API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57c3b-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="57c3b-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="57c3b-123">-PassThru</span></span>
<span data-ttu-id="57c3b-124">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57c3b-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="57c3b-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="57c3b-125">-Confirm</span></span>
<span data-ttu-id="57c3b-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57c3b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c3b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c3b-127">-WhatIf</span></span>
<span data-ttu-id="57c3b-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57c3b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c3b-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57c3b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c3b-130">CommonParameters</span></span>
<span data-ttu-id="57c3b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57c3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c3b-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57c3b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c3b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57c3b-133">INPUTS</span></span>

### <span data-ttu-id="57c3b-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="57c3b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57c3b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="57c3b-135">System.String</span></span>

### <span data-ttu-id="57c3b-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="57c3b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57c3b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57c3b-137">OUTPUTS</span></span>

### <span data-ttu-id="57c3b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57c3b-138">System.Boolean</span></span>

## <span data-ttu-id="57c3b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57c3b-139">NOTES</span></span>

## <span data-ttu-id="57c3b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57c3b-140">RELATED LINKS</span></span>

[<span data-ttu-id="57c3b-141">Get-Azapsananatomentoperation</span><span class="sxs-lookup"><span data-stu-id="57c3b-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="57c3b-142">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="57c3b-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="57c3b-143">Set-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="57c3b-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


