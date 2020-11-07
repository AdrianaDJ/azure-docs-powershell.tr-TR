---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: ff8a4427a909af35d8e8a910210e559212a6b7c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753460"
---
# <span data-ttu-id="25803-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="25803-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="25803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25803-102">SYNOPSIS</span></span>
<span data-ttu-id="25803-103">Bir API yönetim günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25803-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="25803-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25803-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25803-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25803-105">DESCRIPTION</span></span>
<span data-ttu-id="25803-106">**Remove-Azapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25803-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="25803-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25803-107">EXAMPLES</span></span>

### <span data-ttu-id="25803-108">Örnek 1: günlükçü kaldırma</span><span class="sxs-lookup"><span data-stu-id="25803-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="25803-109">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25803-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="25803-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25803-110">PARAMETERS</span></span>

### <span data-ttu-id="25803-111">-Context</span><span class="sxs-lookup"><span data-stu-id="25803-111">-Context</span></span>
<span data-ttu-id="25803-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25803-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="25803-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25803-113">-DefaultProfile</span></span>
<span data-ttu-id="25803-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25803-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25803-115">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="25803-115">-LoggerId</span></span>
<span data-ttu-id="25803-116">Kaldırılacak günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="25803-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="25803-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="25803-117">-PassThru</span></span>
<span data-ttu-id="25803-118">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="25803-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="25803-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="25803-119">-Confirm</span></span>
<span data-ttu-id="25803-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25803-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25803-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25803-121">-WhatIf</span></span>
<span data-ttu-id="25803-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25803-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25803-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25803-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25803-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25803-124">CommonParameters</span></span>
<span data-ttu-id="25803-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25803-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25803-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="25803-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25803-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25803-127">INPUTS</span></span>

### <span data-ttu-id="25803-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="25803-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25803-129">System. String</span><span class="sxs-lookup"><span data-stu-id="25803-129">System.String</span></span>

### <span data-ttu-id="25803-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25803-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25803-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25803-131">OUTPUTS</span></span>

### <span data-ttu-id="25803-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25803-132">System.Boolean</span></span>

## <span data-ttu-id="25803-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25803-133">NOTES</span></span>

## <span data-ttu-id="25803-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25803-134">RELATED LINKS</span></span>

[<span data-ttu-id="25803-135">Get-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="25803-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="25803-136">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="25803-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="25803-137">Set-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="25803-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


