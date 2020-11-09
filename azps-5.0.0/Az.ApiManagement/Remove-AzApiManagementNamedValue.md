---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326044"
---
# <span data-ttu-id="d0b33-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="d0b33-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="d0b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b33-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b33-103">Bir API Yönetimi adlandırılmış değeri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0b33-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="d0b33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0b33-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0b33-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b33-106">**Remove-Azapsananagementnamedvalue** cmdlet 'i, BIR Azure API Yönetimi **adlandırılmış değerini** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0b33-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="d0b33-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0b33-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b33-108">Örnek 1: adlandırılmış değeri kaldırma</span><span class="sxs-lookup"><span data-stu-id="d0b33-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="d0b33-109">Bu komut, Property11 KIMLIĞINE sahip olan adlandırılmış değeri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0b33-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="d0b33-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0b33-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b33-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d0b33-111">-Context</span></span>
<span data-ttu-id="d0b33-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="d0b33-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0b33-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d0b33-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d0b33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b33-114">-DefaultProfile</span></span>
<span data-ttu-id="d0b33-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0b33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b33-116">Namedvalueıd</span><span class="sxs-lookup"><span data-stu-id="d0b33-116">-NamedValueId</span></span>
<span data-ttu-id="d0b33-117">Var olan adlandırılmış değerin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d0b33-117">Identifier of existing named value.</span></span>
<span data-ttu-id="d0b33-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d0b33-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d0b33-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d0b33-119">-PassThru</span></span>
<span data-ttu-id="d0b33-120">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="d0b33-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d0b33-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d0b33-121">This parameter is optional.</span></span>
<span data-ttu-id="d0b33-122">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="d0b33-122">Default value is false.</span></span>

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

### <span data-ttu-id="d0b33-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0b33-123">-Confirm</span></span>
<span data-ttu-id="d0b33-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0b33-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b33-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b33-125">-WhatIf</span></span>
<span data-ttu-id="d0b33-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0b33-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b33-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0b33-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b33-128">CommonParameters</span></span>
<span data-ttu-id="d0b33-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0b33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b33-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d0b33-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b33-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0b33-131">INPUTS</span></span>

### <span data-ttu-id="d0b33-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d0b33-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0b33-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b33-133">System.String</span></span>

### <span data-ttu-id="d0b33-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d0b33-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0b33-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0b33-135">OUTPUTS</span></span>

### <span data-ttu-id="d0b33-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0b33-136">System.Boolean</span></span>

## <span data-ttu-id="d0b33-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0b33-137">NOTES</span></span>

## <span data-ttu-id="d0b33-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0b33-138">RELATED LINKS</span></span>
