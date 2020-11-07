---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: a60f39f6abf81af00e617c454c3af2f8bb682749
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763509"
---
# <span data-ttu-id="599c2-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="599c2-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="599c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="599c2-102">SYNOPSIS</span></span>
<span data-ttu-id="599c2-103">Bir API yönetim özelliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="599c2-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="599c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="599c2-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="599c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="599c2-105">DESCRIPTION</span></span>
<span data-ttu-id="599c2-106">**Remove-Azurermapsananagementproperty** cmdlet 'ı BIR Azure API Yönetim **özelliğini** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="599c2-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="599c2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="599c2-107">EXAMPLES</span></span>

### <span data-ttu-id="599c2-108">Örnek 1: Özellik Kaldırma</span><span class="sxs-lookup"><span data-stu-id="599c2-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="599c2-109">Bu komut, KIMLIK Property11 özelliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="599c2-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="599c2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="599c2-110">PARAMETERS</span></span>

### <span data-ttu-id="599c2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="599c2-111">-Context</span></span>
<span data-ttu-id="599c2-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="599c2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="599c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599c2-113">-DefaultProfile</span></span>
<span data-ttu-id="599c2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="599c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="599c2-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="599c2-115">-PassThru</span></span>
<span data-ttu-id="599c2-116">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="599c2-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="599c2-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="599c2-117">-PropertyId</span></span>
<span data-ttu-id="599c2-118">Bu cmdlet 'in kaldırıldığı özelliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="599c2-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="599c2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="599c2-119">-Confirm</span></span>
<span data-ttu-id="599c2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="599c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="599c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599c2-121">-WhatIf</span></span>
<span data-ttu-id="599c2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="599c2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="599c2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="599c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="599c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599c2-124">CommonParameters</span></span>
<span data-ttu-id="599c2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="599c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599c2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599c2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="599c2-127">INPUTS</span></span>

### <span data-ttu-id="599c2-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="599c2-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="599c2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="599c2-129">System.String</span></span>

### <span data-ttu-id="599c2-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="599c2-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="599c2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="599c2-131">OUTPUTS</span></span>

### <span data-ttu-id="599c2-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="599c2-132">System.Boolean</span></span>

## <span data-ttu-id="599c2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="599c2-133">NOTES</span></span>

## <span data-ttu-id="599c2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="599c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="599c2-135">New-Azurermapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="599c2-135">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="599c2-136">Set-Azurermapımanagementproperty</span><span class="sxs-lookup"><span data-stu-id="599c2-136">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


