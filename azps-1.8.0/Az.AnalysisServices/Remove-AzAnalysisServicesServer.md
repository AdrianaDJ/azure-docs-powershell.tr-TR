---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: b64ba86a6aab80910ac09bd3757565df433690dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751203"
---
# <span data-ttu-id="d963c-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d963c-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d963c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d963c-102">SYNOPSIS</span></span>
<span data-ttu-id="d963c-103">Analysis Services sunucusunun bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="d963c-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d963c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d963c-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d963c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d963c-105">DESCRIPTION</span></span>
<span data-ttu-id="d963c-106">Remove-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="d963c-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d963c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d963c-107">EXAMPLES</span></span>

### <span data-ttu-id="d963c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d963c-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d963c-109">Bu komut, resourcegroup testgroup 'da TestServer adlı sunucuyu kaldıracak</span><span class="sxs-lookup"><span data-stu-id="d963c-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d963c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d963c-110">PARAMETERS</span></span>

### <span data-ttu-id="d963c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d963c-111">-DefaultProfile</span></span>
<span data-ttu-id="d963c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d963c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d963c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d963c-113">-Name</span></span>
<span data-ttu-id="d963c-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="d963c-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d963c-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d963c-115">-PassThru</span></span>
<span data-ttu-id="d963c-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="d963c-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d963c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d963c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d963c-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d963c-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d963c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d963c-119">-Confirm</span></span>
<span data-ttu-id="d963c-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="d963c-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d963c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d963c-121">-WhatIf</span></span>
<span data-ttu-id="d963c-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="d963c-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d963c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d963c-123">CommonParameters</span></span>
<span data-ttu-id="d963c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d963c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d963c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d963c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d963c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d963c-126">INPUTS</span></span>

### <span data-ttu-id="d963c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d963c-127">System.String</span></span>

## <span data-ttu-id="d963c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d963c-128">OUTPUTS</span></span>

### <span data-ttu-id="d963c-129">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d963c-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d963c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d963c-130">NOTES</span></span>
<span data-ttu-id="d963c-131">Diğer ad: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="d963c-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="d963c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d963c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d963c-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d963c-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d963c-134">Yeni-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d963c-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)