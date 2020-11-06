---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 135dced6c66f1212f172a2c435a7468b16e71708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573037"
---
# <span data-ttu-id="fb637-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fb637-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="fb637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb637-102">SYNOPSIS</span></span>
<span data-ttu-id="fb637-103">Bir API yönetim günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb637-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb637-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb637-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb637-105">DESCRIPTION</span></span>
<span data-ttu-id="fb637-106">**Remove-Azurermapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb637-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="fb637-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb637-107">EXAMPLES</span></span>

### <span data-ttu-id="fb637-108">Örnek 1: günlükçü kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb637-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="fb637-109">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb637-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="fb637-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb637-110">PARAMETERS</span></span>

### <span data-ttu-id="fb637-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fb637-111">-Context</span></span>
<span data-ttu-id="fb637-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb637-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fb637-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb637-113">-DefaultProfile</span></span>
<span data-ttu-id="fb637-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb637-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb637-115">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="fb637-115">-LoggerId</span></span>
<span data-ttu-id="fb637-116">Kaldırılacak günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb637-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="fb637-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb637-117">-PassThru</span></span>
<span data-ttu-id="fb637-118">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="fb637-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="fb637-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb637-119">-Confirm</span></span>
<span data-ttu-id="fb637-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb637-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb637-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb637-121">-WhatIf</span></span>
<span data-ttu-id="fb637-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb637-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb637-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb637-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb637-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb637-124">CommonParameters</span></span>
<span data-ttu-id="fb637-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb637-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb637-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb637-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb637-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb637-127">INPUTS</span></span>

### <span data-ttu-id="fb637-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fb637-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fb637-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fb637-129">System.String</span></span>

### <span data-ttu-id="fb637-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb637-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb637-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb637-131">OUTPUTS</span></span>

### <span data-ttu-id="fb637-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb637-132">System.Boolean</span></span>

## <span data-ttu-id="fb637-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb637-133">NOTES</span></span>

## <span data-ttu-id="fb637-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb637-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb637-135">Get-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="fb637-135">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="fb637-136">Yeni-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="fb637-136">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="fb637-137">Set-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="fb637-137">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


