---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 5729daec656c7f99ac7f4c4c9440e090217c315d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590696"
---
# <span data-ttu-id="aca1f-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="aca1f-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="aca1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca1f-102">SYNOPSIS</span></span>
<span data-ttu-id="aca1f-103">Linux bilgisayarlara veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="aca1f-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aca1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aca1f-104">SYNTAX</span></span>

### <span data-ttu-id="aca1f-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aca1f-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aca1f-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="aca1f-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aca1f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aca1f-107">DESCRIPTION</span></span>
<span data-ttu-id="aca1f-108">**Yeni-Azurermoperationalınsightslinuxsyslogdatasource** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarına bir Syslog veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="aca1f-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="aca1f-109">Azure Operasyonel Öngörüler, syslog verileri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="aca1f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aca1f-110">EXAMPLES</span></span>

## <span data-ttu-id="aca1f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aca1f-111">PARAMETERS</span></span>

### <span data-ttu-id="aca1f-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="aca1f-112">-CollectAlert</span></span>
<span data-ttu-id="aca1f-113">Işlemsel öngörülerle uyarı mesajları topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="aca1f-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="aca1f-114">-CollectCritical</span></span>
<span data-ttu-id="aca1f-115">Işlemsel öngörülerle önemli iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="aca1f-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="aca1f-116">-CollectDebug</span></span>
<span data-ttu-id="aca1f-117">Işlemsel öngörülerle hata ayıklama iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="aca1f-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="aca1f-118">-CollectEmergency</span></span>
<span data-ttu-id="aca1f-119">Işlemsel Öngörüler 'in acil durum iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="aca1f-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="aca1f-120">-CollectError</span></span>
<span data-ttu-id="aca1f-121">Işlemsel öngörülerle hata iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="aca1f-122">-Collectbilgilendirme</span><span class="sxs-lookup"><span data-stu-id="aca1f-122">-CollectInformational</span></span>
<span data-ttu-id="aca1f-123">Işlemsel Öngörüler 'in bilgilendirici iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="aca1f-124">-Collectbildirimi</span><span class="sxs-lookup"><span data-stu-id="aca1f-124">-CollectNotice</span></span>
<span data-ttu-id="aca1f-125">Işlemsel öngörülerle bildirim iletileri topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="aca1f-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="aca1f-126">-CollectWarning</span></span>
<span data-ttu-id="aca1f-127">Syslog, uyarı mesajları içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="aca1f-128">-Tesis</span><span class="sxs-lookup"><span data-stu-id="aca1f-128">-Facility</span></span>
<span data-ttu-id="aca1f-129">Bir tesis kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-129">Specifies a facility code.</span></span>

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

### <span data-ttu-id="aca1f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="aca1f-130">-Force</span></span>
<span data-ttu-id="aca1f-131">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="aca1f-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aca1f-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="aca1f-132">-Name</span></span>
<span data-ttu-id="aca1f-133">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-133">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="aca1f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca1f-134">-ResourceGroupName</span></span>
<span data-ttu-id="aca1f-135">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-135">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="aca1f-136">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="aca1f-136">-Workspace</span></span>
<span data-ttu-id="aca1f-137">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-137">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aca1f-138">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="aca1f-138">-WorkspaceName</span></span>
<span data-ttu-id="aca1f-139">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-139">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aca1f-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="aca1f-140">-Confirm</span></span>
<span data-ttu-id="aca1f-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aca1f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca1f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca1f-142">-WhatIf</span></span>
<span data-ttu-id="aca1f-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aca1f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca1f-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aca1f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aca1f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca1f-145">-DefaultProfile</span></span>
<span data-ttu-id="aca1f-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aca1f-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aca1f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca1f-147">CommonParameters</span></span>
<span data-ttu-id="aca1f-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aca1f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca1f-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca1f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca1f-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aca1f-150">INPUTS</span></span>

### <span data-ttu-id="aca1f-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aca1f-151">PSWorkspace</span></span>
<span data-ttu-id="aca1f-152">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aca1f-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="aca1f-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aca1f-153">OUTPUTS</span></span>

### <span data-ttu-id="aca1f-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="aca1f-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="aca1f-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aca1f-155">NOTES</span></span>

## <span data-ttu-id="aca1f-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aca1f-156">RELATED LINKS</span></span>

[<span data-ttu-id="aca1f-157">Disable-Azurermoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="aca1f-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="aca1f-158">Enable-Azurermoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="aca1f-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


