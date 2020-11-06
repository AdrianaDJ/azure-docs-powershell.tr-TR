---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: fb55eec3dc0bf3cf83032251e017749a07970f2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587053"
---
# <span data-ttu-id="ae778-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ae778-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="ae778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae778-102">SYNOPSIS</span></span>
<span data-ttu-id="ae778-103">Analysis Services sunucusunun bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="ae778-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae778-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae778-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae778-105">DESCRIPTION</span></span>
<span data-ttu-id="ae778-106">Remove-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="ae778-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="ae778-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae778-107">EXAMPLES</span></span>

### <span data-ttu-id="ae778-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae778-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="ae778-109">Bu komut, resourcegroup testgroup 'da TestServer adlı sunucuyu kaldıracak</span><span class="sxs-lookup"><span data-stu-id="ae778-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="ae778-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae778-110">PARAMETERS</span></span>

### <span data-ttu-id="ae778-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae778-111">-Name</span></span>
<span data-ttu-id="ae778-112">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="ae778-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ae778-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ae778-113">-PassThru</span></span>
<span data-ttu-id="ae778-114">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="ae778-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="ae778-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae778-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae778-116">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ae778-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="ae778-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae778-117">-Confirm</span></span>
<span data-ttu-id="ae778-118">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="ae778-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="ae778-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae778-119">-WhatIf</span></span>
<span data-ttu-id="ae778-120">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="ae778-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="ae778-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae778-121">-DefaultProfile</span></span>
<span data-ttu-id="ae778-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae778-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae778-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae778-123">CommonParameters</span></span>
<span data-ttu-id="ae778-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae778-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae778-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae778-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae778-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae778-126">INPUTS</span></span>

## <span data-ttu-id="ae778-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae778-127">OUTPUTS</span></span>

### <span data-ttu-id="ae778-128">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ae778-128">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="ae778-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae778-129">NOTES</span></span>
<span data-ttu-id="ae778-130">Diğer ad: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="ae778-130">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="ae778-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae778-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae778-132">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ae778-132">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="ae778-133">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ae778-133">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
