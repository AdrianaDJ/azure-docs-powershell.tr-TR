---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592678"
---
# <span data-ttu-id="f0be0-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f0be0-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f0be0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0be0-102">SYNOPSIS</span></span>
<span data-ttu-id="f0be0-103">Otomasyon 'daki DSC derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0be0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0be0-104">SYNTAX</span></span>

### <span data-ttu-id="f0be0-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0be0-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0be0-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="f0be0-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0be0-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f0be0-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0be0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0be0-108">DESCRIPTION</span></span>
<span data-ttu-id="f0be0-109">**Get-AzureRmAutomationDscCompilationJob** cmdlet 'i, Mac OTOMASYONUNDA APS Istenen durum yapılandırma (DSC) derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="f0be0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0be0-110">EXAMPLES</span></span>

### <span data-ttu-id="f0be0-111">Örnek 1: tüm DSC derleme işlerini al</span><span class="sxs-lookup"><span data-stu-id="f0be0-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f0be0-112">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f0be0-113">Örnek 2: bir yapılandırma için DSC derleme işlerini alma</span><span class="sxs-lookup"><span data-stu-id="f0be0-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f0be0-114">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConfiguration adlı DSC yapılandırmasına yönelik tüm derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f0be0-115">Örnek 3: belirli bir DSC derleme işi edinme</span><span class="sxs-lookup"><span data-stu-id="f0be0-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="f0be0-116">Bu komut, Contoso17 adlı Otomasyon hesabında belirtilen KIMLIĞE sahip derleme işini alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f0be0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0be0-117">PARAMETERS</span></span>

### <span data-ttu-id="f0be0-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0be0-118">-AutomationAccountName</span></span>
<span data-ttu-id="f0be0-119">Bu cmdlet 'in aldığı DSC derleme işlerini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0be0-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f0be0-120">-ConfigurationName</span></span>
<span data-ttu-id="f0be0-121">Bu cmdlet 'in derleme işlerini aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0be0-122">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="f0be0-122">-EndTime</span></span>
<span data-ttu-id="f0be0-123">Bitiş saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-123">Specifies an end time.</span></span>
<span data-ttu-id="f0be0-124">Bu cmdlet, bu parametrenin belirttiği zamana kadar başlatılan derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0be0-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f0be0-125">-Id</span></span>
<span data-ttu-id="f0be0-126">Bu cmdlet 'in aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0be0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0be0-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0be0-128">Bu cmdlet 'in DSC derleme işlerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="f0be0-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="f0be0-129">-StartTime</span></span>
<span data-ttu-id="f0be0-130">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-130">Specifies a start time.</span></span>
<span data-ttu-id="f0be0-131">Bu cmdlet, bu parametrenin belirttiği zamandan sonraki veya sonraki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="f0be0-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0be0-132">-Durum</span><span class="sxs-lookup"><span data-stu-id="f0be0-132">-Status</span></span>
<span data-ttu-id="f0be0-133">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0be0-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f0be0-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f0be0-134">Valid values are:</span></span> 

- <span data-ttu-id="f0be0-135">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="f0be0-135">Completed</span></span> 
- <span data-ttu-id="f0be0-136">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="f0be0-136">Failed</span></span> 
- <span data-ttu-id="f0be0-137">Sıradan</span><span class="sxs-lookup"><span data-stu-id="f0be0-137">Queued</span></span> 
- <span data-ttu-id="f0be0-138">Başlarken</span><span class="sxs-lookup"><span data-stu-id="f0be0-138">Starting</span></span> 
- <span data-ttu-id="f0be0-139">İlirken</span><span class="sxs-lookup"><span data-stu-id="f0be0-139">Resuming</span></span> 
- <span data-ttu-id="f0be0-140">Çalışması</span><span class="sxs-lookup"><span data-stu-id="f0be0-140">Running</span></span> 
- <span data-ttu-id="f0be0-141">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="f0be0-141">Stopped</span></span> 
- <span data-ttu-id="f0be0-142">Arak</span><span class="sxs-lookup"><span data-stu-id="f0be0-142">Stopping</span></span> 
- <span data-ttu-id="f0be0-143">Etsin</span><span class="sxs-lookup"><span data-stu-id="f0be0-143">Suspended</span></span> 
- <span data-ttu-id="f0be0-144">Et</span><span class="sxs-lookup"><span data-stu-id="f0be0-144">Suspending</span></span> 
- <span data-ttu-id="f0be0-145">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="f0be0-145">Activating</span></span>
- <span data-ttu-id="f0be0-146">Yeni</span><span class="sxs-lookup"><span data-stu-id="f0be0-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0be0-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0be0-147">-DefaultProfile</span></span>
<span data-ttu-id="f0be0-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0be0-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0be0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0be0-149">CommonParameters</span></span>
<span data-ttu-id="f0be0-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0be0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0be0-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0be0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0be0-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0be0-152">INPUTS</span></span>

## <span data-ttu-id="f0be0-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0be0-153">OUTPUTS</span></span>

### <span data-ttu-id="f0be0-154">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f0be0-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f0be0-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0be0-155">NOTES</span></span>

## <span data-ttu-id="f0be0-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0be0-156">RELATED LINKS</span></span>

[<span data-ttu-id="f0be0-157">Get-Azurermautomationdsccompilationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="f0be0-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="f0be0-158">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f0be0-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


