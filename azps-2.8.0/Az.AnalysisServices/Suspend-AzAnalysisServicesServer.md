---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: ecd9e83607da048246ec996188fd9a31d231ff32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753629"
---
# <span data-ttu-id="20c27-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20c27-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="20c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c27-102">SYNOPSIS</span></span>
<span data-ttu-id="20c27-103">Analysis Services sunucusu örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="20c27-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="20c27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20c27-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20c27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20c27-105">DESCRIPTION</span></span>
<span data-ttu-id="20c27-106">Suspend-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="20c27-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="20c27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20c27-107">EXAMPLES</span></span>

### <span data-ttu-id="20c27-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="20c27-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="20c27-109">Bu komut, resourcegroup test grubunda TestServer adlı etkin bir sunucuyu askıya alacaktır</span><span class="sxs-lookup"><span data-stu-id="20c27-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="20c27-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20c27-110">PARAMETERS</span></span>

### <span data-ttu-id="20c27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c27-111">-DefaultProfile</span></span>
<span data-ttu-id="20c27-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20c27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20c27-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="20c27-113">-Name</span></span>
<span data-ttu-id="20c27-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="20c27-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="20c27-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20c27-115">-PassThru</span></span>
<span data-ttu-id="20c27-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="20c27-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="20c27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c27-117">-ResourceGroupName</span></span>
<span data-ttu-id="20c27-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="20c27-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="20c27-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="20c27-119">-Confirm</span></span>
<span data-ttu-id="20c27-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="20c27-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="20c27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20c27-121">-WhatIf</span></span>
<span data-ttu-id="20c27-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="20c27-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="20c27-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c27-123">CommonParameters</span></span>
<span data-ttu-id="20c27-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20c27-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c27-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c27-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c27-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20c27-126">INPUTS</span></span>

### <span data-ttu-id="20c27-127">System. String</span><span class="sxs-lookup"><span data-stu-id="20c27-127">System.String</span></span>

## <span data-ttu-id="20c27-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20c27-128">OUTPUTS</span></span>

### <span data-ttu-id="20c27-129">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20c27-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="20c27-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20c27-130">NOTES</span></span>
<span data-ttu-id="20c27-131">Diğer ad: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="20c27-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="20c27-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20c27-132">RELATED LINKS</span></span>

[<span data-ttu-id="20c27-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20c27-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="20c27-134">Özgeçmiş-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20c27-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

