---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759844"
---
# <span data-ttu-id="2575e-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="2575e-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="2575e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2575e-102">SYNOPSIS</span></span>
<span data-ttu-id="2575e-103">Linux bilgisayarlara veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="2575e-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="2575e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2575e-104">SYNTAX</span></span>

### <span data-ttu-id="2575e-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2575e-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2575e-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="2575e-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2575e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2575e-107">DESCRIPTION</span></span>
<span data-ttu-id="2575e-108">**New-Azoperationalınsightslinuxsyslogdatasource** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarına bir Syslog veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="2575e-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="2575e-109">Azure Operasyonel Öngörüler, syslog verileri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="2575e-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="2575e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2575e-110">EXAMPLES</span></span>

## <span data-ttu-id="2575e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2575e-111">PARAMETERS</span></span>

### <span data-ttu-id="2575e-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="2575e-112">-CollectAlert</span></span>
<span data-ttu-id="2575e-113">Işlemsel öngörülerle uyarı mesajları topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="2575e-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="2575e-114">-CollectCritical</span></span>
<span data-ttu-id="2575e-115">Işlemsel öngörülerle önemli iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="2575e-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="2575e-116">-CollectDebug</span></span>
<span data-ttu-id="2575e-117">Işlemsel öngörülerle hata ayıklama iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="2575e-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="2575e-118">-CollectEmergency</span></span>
<span data-ttu-id="2575e-119">Işlemsel Öngörüler 'in acil durum iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="2575e-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="2575e-120">-CollectError</span></span>
<span data-ttu-id="2575e-121">Işlemsel öngörülerle hata iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="2575e-122">-Collectbilgilendirme</span><span class="sxs-lookup"><span data-stu-id="2575e-122">-CollectInformational</span></span>
<span data-ttu-id="2575e-123">Işlemsel Öngörüler 'in bilgilendirici iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="2575e-124">-Collectbildirimi</span><span class="sxs-lookup"><span data-stu-id="2575e-124">-CollectNotice</span></span>
<span data-ttu-id="2575e-125">Işlemsel öngörülerle bildirim iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2575e-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="2575e-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="2575e-126">-CollectWarning</span></span>
<span data-ttu-id="2575e-127">Syslog, uyarı mesajları içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2575e-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="2575e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2575e-128">-DefaultProfile</span></span>
<span data-ttu-id="2575e-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2575e-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2575e-130">-Tesis</span><span class="sxs-lookup"><span data-stu-id="2575e-130">-Facility</span></span>
<span data-ttu-id="2575e-131">Bir tesis kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2575e-131">Specifies a facility code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2575e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="2575e-132">-Force</span></span>
<span data-ttu-id="2575e-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2575e-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2575e-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="2575e-134">-Name</span></span>
<span data-ttu-id="2575e-135">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="2575e-135">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2575e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2575e-136">-ResourceGroupName</span></span>
<span data-ttu-id="2575e-137">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2575e-137">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2575e-138">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="2575e-138">-Workspace</span></span>
<span data-ttu-id="2575e-139">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2575e-139">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2575e-140">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="2575e-140">-WorkspaceName</span></span>
<span data-ttu-id="2575e-141">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2575e-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2575e-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="2575e-142">-Confirm</span></span>
<span data-ttu-id="2575e-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2575e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2575e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2575e-144">-WhatIf</span></span>
<span data-ttu-id="2575e-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2575e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2575e-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2575e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2575e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2575e-147">CommonParameters</span></span>
<span data-ttu-id="2575e-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2575e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2575e-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2575e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2575e-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2575e-150">INPUTS</span></span>

### <span data-ttu-id="2575e-151">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2575e-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2575e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2575e-152">System.String</span></span>

## <span data-ttu-id="2575e-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2575e-153">OUTPUTS</span></span>

### <span data-ttu-id="2575e-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="2575e-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2575e-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2575e-155">NOTES</span></span>

## <span data-ttu-id="2575e-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2575e-156">RELATED LINKS</span></span>

[<span data-ttu-id="2575e-157">Disable-Azoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="2575e-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="2575e-158">Enable-Azoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="2575e-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


