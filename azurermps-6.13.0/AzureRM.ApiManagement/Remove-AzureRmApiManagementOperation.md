---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1a3fd2ca25099be029616e048c5ebfa0e398229e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573041"
---
# <span data-ttu-id="ad282-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ad282-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ad282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad282-102">SYNOPSIS</span></span>
<span data-ttu-id="ad282-103">Var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ad282-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad282-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad282-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad282-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad282-105">DESCRIPTION</span></span>
<span data-ttu-id="ad282-106">**Remove-Azurermapsananagementoperation** cmdlet 'i var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ad282-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="ad282-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad282-107">EXAMPLES</span></span>

### <span data-ttu-id="ad282-108">Örnek 1: var olan bir API Işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ad282-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="ad282-109">Bu komut, var olan bir API Işlemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ad282-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="ad282-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad282-110">PARAMETERS</span></span>

### <span data-ttu-id="ad282-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="ad282-111">-ApiId</span></span>
<span data-ttu-id="ad282-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad282-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ad282-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="ad282-113">-ApiRevision</span></span>
<span data-ttu-id="ad282-114">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="ad282-114">Identifier of API Revision.</span></span> <span data-ttu-id="ad282-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ad282-115">This parameter is optional.</span></span> <span data-ttu-id="ad282-116">Belirtilmezse, işlem geçerli API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="ad282-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="ad282-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ad282-117">-Context</span></span>
<span data-ttu-id="ad282-118">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad282-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ad282-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad282-119">-DefaultProfile</span></span>
<span data-ttu-id="ad282-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad282-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad282-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ad282-121">-OperationId</span></span>
<span data-ttu-id="ad282-122">API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad282-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="ad282-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ad282-123">-PassThru</span></span>
<span data-ttu-id="ad282-124">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad282-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ad282-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad282-125">-Confirm</span></span>
<span data-ttu-id="ad282-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad282-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad282-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad282-127">-WhatIf</span></span>
<span data-ttu-id="ad282-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad282-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad282-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad282-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad282-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad282-130">CommonParameters</span></span>
<span data-ttu-id="ad282-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad282-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad282-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad282-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad282-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad282-133">INPUTS</span></span>

### <span data-ttu-id="ad282-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ad282-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad282-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ad282-135">System.String</span></span>

### <span data-ttu-id="ad282-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ad282-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ad282-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad282-137">OUTPUTS</span></span>

### <span data-ttu-id="ad282-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad282-138">System.Boolean</span></span>

## <span data-ttu-id="ad282-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad282-139">NOTES</span></span>

## <span data-ttu-id="ad282-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad282-140">RELATED LINKS</span></span>

[<span data-ttu-id="ad282-141">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="ad282-141">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ad282-142">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="ad282-142">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ad282-143">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="ad282-143">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


