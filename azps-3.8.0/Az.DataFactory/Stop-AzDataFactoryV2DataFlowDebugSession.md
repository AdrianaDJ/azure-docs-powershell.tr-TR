---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938270"
---
# <span data-ttu-id="4468a-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4468a-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="4468a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4468a-102">SYNOPSIS</span></span>
<span data-ttu-id="4468a-103">Azure Veri Fabrikası 'nde veri akışı hata ayıklama oturumunu durdurur</span><span class="sxs-lookup"><span data-stu-id="4468a-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="4468a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4468a-104">SYNTAX</span></span>

### <span data-ttu-id="4468a-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4468a-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4468a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4468a-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4468a-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4468a-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4468a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4468a-108">DESCRIPTION</span></span>
<span data-ttu-id="4468a-109">Bu komut, yoksa, hata ayıklama oturumunun canlı ayarına göre oturum otomatik olarak kapatılır.</span><span class="sxs-lookup"><span data-stu-id="4468a-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="4468a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4468a-110">EXAMPLES</span></span>

### <span data-ttu-id="4468a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4468a-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="4468a-112">"WikiADF" Veri Fabrikası</span><span class="sxs-lookup"><span data-stu-id="4468a-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="4468a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4468a-113">PARAMETERS</span></span>

### <span data-ttu-id="4468a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4468a-114">-DataFactory</span></span>
<span data-ttu-id="4468a-115">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4468a-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4468a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4468a-116">-DataFactoryName</span></span>
<span data-ttu-id="4468a-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="4468a-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4468a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4468a-118">-DefaultProfile</span></span>
<span data-ttu-id="4468a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4468a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4468a-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4468a-120">-PassThru</span></span>
<span data-ttu-id="4468a-121">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="4468a-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="4468a-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4468a-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="4468a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4468a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4468a-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4468a-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4468a-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4468a-125">-ResourceId</span></span>
<span data-ttu-id="4468a-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4468a-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4468a-127">-SessionID</span><span class="sxs-lookup"><span data-stu-id="4468a-127">-SessionId</span></span>
<span data-ttu-id="4468a-128">Veri akışı hata ayıklama oturum KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4468a-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4468a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="4468a-129">-Confirm</span></span>
<span data-ttu-id="4468a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4468a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4468a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4468a-131">-WhatIf</span></span>
<span data-ttu-id="4468a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4468a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4468a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4468a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4468a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4468a-134">CommonParameters</span></span>
<span data-ttu-id="4468a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4468a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4468a-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4468a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4468a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4468a-137">INPUTS</span></span>

### <span data-ttu-id="4468a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4468a-138">System.String</span></span>

### <span data-ttu-id="4468a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="4468a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4468a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4468a-140">OUTPUTS</span></span>

### <span data-ttu-id="4468a-141">System. void</span><span class="sxs-lookup"><span data-stu-id="4468a-141">System.Void</span></span>

### <span data-ttu-id="4468a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4468a-142">System.Boolean</span></span>

## <span data-ttu-id="4468a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4468a-143">NOTES</span></span>
<span data-ttu-id="4468a-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="4468a-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4468a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4468a-145">RELATED LINKS</span></span>

[<span data-ttu-id="4468a-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4468a-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="4468a-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4468a-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="4468a-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="4468a-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="4468a-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="4468a-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)