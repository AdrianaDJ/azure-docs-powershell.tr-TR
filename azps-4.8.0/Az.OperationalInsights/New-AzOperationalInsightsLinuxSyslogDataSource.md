---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109417"
---
# <span data-ttu-id="56270-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="56270-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="56270-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56270-102">SYNOPSIS</span></span>
<span data-ttu-id="56270-103">Linux bilgisayarlara veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="56270-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="56270-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56270-104">SYNTAX</span></span>

### <span data-ttu-id="56270-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56270-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56270-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="56270-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56270-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="56270-107">DESCRIPTION</span></span>
<span data-ttu-id="56270-108">**New-Azoperationalınsightslinuxsyslogdatasource** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarına bir Syslog veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="56270-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="56270-109">Azure Operasyonel Öngörüler, syslog verileri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="56270-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="56270-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56270-110">EXAMPLES</span></span>

### <span data-ttu-id="56270-111">Örnek 1: Syslog veri kaynakları oluşturma</span><span class="sxs-lookup"><span data-stu-id="56270-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="56270-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56270-112">PARAMETERS</span></span>

### <span data-ttu-id="56270-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="56270-113">-CollectAlert</span></span>
<span data-ttu-id="56270-114">Işlemsel öngörülerle uyarı mesajları topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="56270-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="56270-115">-CollectCritical</span></span>
<span data-ttu-id="56270-116">Işlemsel öngörülerle önemli iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="56270-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="56270-117">-CollectDebug</span></span>
<span data-ttu-id="56270-118">Işlemsel öngörülerle hata ayıklama iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="56270-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="56270-119">-CollectEmergency</span></span>
<span data-ttu-id="56270-120">Işlemsel Öngörüler 'in acil durum iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="56270-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="56270-121">-CollectError</span></span>
<span data-ttu-id="56270-122">Işlemsel öngörülerle hata iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="56270-123">-Collectbilgilendirme</span><span class="sxs-lookup"><span data-stu-id="56270-123">-CollectInformational</span></span>
<span data-ttu-id="56270-124">Işlemsel Öngörüler 'in bilgilendirici iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="56270-125">-Collectbildirimi</span><span class="sxs-lookup"><span data-stu-id="56270-125">-CollectNotice</span></span>
<span data-ttu-id="56270-126">Işlemsel öngörülerle bildirim iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="56270-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="56270-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="56270-127">-CollectWarning</span></span>
<span data-ttu-id="56270-128">Syslog, uyarı mesajları içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="56270-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="56270-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56270-129">-DefaultProfile</span></span>
<span data-ttu-id="56270-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="56270-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56270-131">-Tesis</span><span class="sxs-lookup"><span data-stu-id="56270-131">-Facility</span></span>
<span data-ttu-id="56270-132">Bir tesis kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="56270-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="56270-133">-Force</span><span class="sxs-lookup"><span data-stu-id="56270-133">-Force</span></span>
<span data-ttu-id="56270-134">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="56270-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56270-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="56270-135">-Name</span></span>
<span data-ttu-id="56270-136">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="56270-136">Specifies a name for the data source.</span></span> <span data-ttu-id="56270-137">Ad, Azure portalında gösterilmez ve tüm dizeler benzersiz olduğu sürece kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="56270-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="56270-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56270-138">-ResourceGroupName</span></span>
<span data-ttu-id="56270-139">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56270-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="56270-140">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="56270-140">-Workspace</span></span>
<span data-ttu-id="56270-141">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56270-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="56270-142">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="56270-142">-WorkspaceName</span></span>
<span data-ttu-id="56270-143">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56270-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="56270-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="56270-144">-Confirm</span></span>
<span data-ttu-id="56270-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56270-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56270-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56270-146">-WhatIf</span></span>
<span data-ttu-id="56270-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56270-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56270-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56270-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56270-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56270-149">CommonParameters</span></span>
<span data-ttu-id="56270-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56270-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56270-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56270-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56270-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56270-152">INPUTS</span></span>

### <span data-ttu-id="56270-153">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="56270-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="56270-154">System. String</span><span class="sxs-lookup"><span data-stu-id="56270-154">System.String</span></span>

## <span data-ttu-id="56270-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56270-155">OUTPUTS</span></span>

### <span data-ttu-id="56270-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="56270-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="56270-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56270-157">NOTES</span></span>

## <span data-ttu-id="56270-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56270-158">RELATED LINKS</span></span>

[<span data-ttu-id="56270-159">Disable-Azoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="56270-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="56270-160">Enable-Azoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="56270-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


