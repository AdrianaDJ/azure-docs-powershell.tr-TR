---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588314"
---
# <span data-ttu-id="69a0f-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="69a0f-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="69a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="69a0f-103">Bir API yönetim günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69a0f-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69a0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69a0f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="69a0f-106">**Remove-Azurermapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69a0f-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="69a0f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="69a0f-108">Örnek 1: günlükçü kaldırma</span><span class="sxs-lookup"><span data-stu-id="69a0f-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="69a0f-109">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69a0f-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="69a0f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="69a0f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="69a0f-111">-Context</span></span>
<span data-ttu-id="69a0f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a0f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="69a0f-113">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="69a0f-113">-LoggerId</span></span>
<span data-ttu-id="69a0f-114">Kaldırılacak günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a0f-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="69a0f-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="69a0f-115">-PassThru</span></span>
<span data-ttu-id="69a0f-116">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="69a0f-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="69a0f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="69a0f-117">-Confirm</span></span>
<span data-ttu-id="69a0f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69a0f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a0f-119">-WhatIf</span></span>
<span data-ttu-id="69a0f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69a0f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a0f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69a0f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a0f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a0f-122">-DefaultProfile</span></span>
<span data-ttu-id="69a0f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69a0f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69a0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a0f-124">CommonParameters</span></span>
<span data-ttu-id="69a0f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69a0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a0f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a0f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a0f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69a0f-127">INPUTS</span></span>

## <span data-ttu-id="69a0f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69a0f-128">OUTPUTS</span></span>

### <span data-ttu-id="69a0f-129">Boole</span><span class="sxs-lookup"><span data-stu-id="69a0f-129">Boolean</span></span>

## <span data-ttu-id="69a0f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69a0f-130">NOTES</span></span>

## <span data-ttu-id="69a0f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69a0f-131">RELATED LINKS</span></span>

[<span data-ttu-id="69a0f-132">Get-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="69a0f-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="69a0f-133">Yeni-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="69a0f-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="69a0f-134">Set-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="69a0f-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


