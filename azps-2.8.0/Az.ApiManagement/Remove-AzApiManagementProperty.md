---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 323cbbdc38281c9b90ab3728eb2879bf1b7bfe89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753447"
---
# <span data-ttu-id="88ea4-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="88ea4-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="88ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="88ea4-103">Bir API yönetim özelliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88ea4-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="88ea4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88ea4-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ea4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="88ea4-106">**Remove-Azapsananagementproperty** cmdlet 'ı BIR Azure API Yönetim **özelliğini** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88ea4-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="88ea4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="88ea4-108">Örnek 1: Özellik Kaldırma</span><span class="sxs-lookup"><span data-stu-id="88ea4-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="88ea4-109">Bu komut, KIMLIK Property11 özelliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88ea4-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="88ea4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="88ea4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="88ea4-111">-Context</span></span>
<span data-ttu-id="88ea4-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ea4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="88ea4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ea4-113">-DefaultProfile</span></span>
<span data-ttu-id="88ea4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88ea4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ea4-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="88ea4-115">-PassThru</span></span>
<span data-ttu-id="88ea4-116">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="88ea4-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="88ea4-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="88ea4-117">-PropertyId</span></span>
<span data-ttu-id="88ea4-118">Bu cmdlet 'in kaldırıldığı özelliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ea4-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88ea4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="88ea4-119">-Confirm</span></span>
<span data-ttu-id="88ea4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88ea4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88ea4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ea4-121">-WhatIf</span></span>
<span data-ttu-id="88ea4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88ea4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88ea4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88ea4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88ea4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ea4-124">CommonParameters</span></span>
<span data-ttu-id="88ea4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88ea4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ea4-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88ea4-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ea4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88ea4-127">INPUTS</span></span>

### <span data-ttu-id="88ea4-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="88ea4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="88ea4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="88ea4-129">System.String</span></span>

### <span data-ttu-id="88ea4-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88ea4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88ea4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88ea4-131">OUTPUTS</span></span>

### <span data-ttu-id="88ea4-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88ea4-132">System.Boolean</span></span>

## <span data-ttu-id="88ea4-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88ea4-133">NOTES</span></span>

## <span data-ttu-id="88ea4-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88ea4-134">RELATED LINKS</span></span>

[<span data-ttu-id="88ea4-135">New-Azapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="88ea4-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="88ea4-136">Set-Azapsananagementözelliği</span><span class="sxs-lookup"><span data-stu-id="88ea4-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


