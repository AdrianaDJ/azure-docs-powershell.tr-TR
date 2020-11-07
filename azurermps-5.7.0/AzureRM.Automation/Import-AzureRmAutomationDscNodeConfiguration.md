---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: cef704c9ab09a17ffe91d3a1541e39df1e943964
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762042"
---
# <span data-ttu-id="6b2ab-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b2ab-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="6b2ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2ab-103">Bir MOF belgesini Otomasyonda DSC düğüm yapılandırması olarak içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b2ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b2ab-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b2ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b2ab-105">DESCRIPTION</span></span>
<span data-ttu-id="6b2ab-106">**Import-AzureRmAutomationDscConfiguration** cmdlet 'ı, yönetilen nesne BIÇIMI (MOF) yapılandırma belgesini Istenen durum yapılandırma (DSC) düğüm yapılandırması olarak Azure Otomasyonu içine aktarır.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="6b2ab-107">. Mof dosyasının yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="6b2ab-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b2ab-108">EXAMPLES</span></span>

### <span data-ttu-id="6b2ab-109">Örnek 1: DSC düğüm yapılandırmasını otomasyona aktarma</span><span class="sxs-lookup"><span data-stu-id="6b2ab-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="6b2ab-110">Bu komut, WebSunucusu. mof adındaki Otomasyon hesabına WebSunucusu. mof adlı dosyadan DSC</span><span class="sxs-lookup"><span data-stu-id="6b2ab-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="6b2ab-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6b2ab-112">ContosoConfiguration. webserver adlı bir DSC düğüm yapılandırması varsa bu komut bunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="6b2ab-113">Örnek 2: bir DSC düğüm yapılandırmasını otomatikleştirme 'ye aktarın ve yeni bir derleme sürümü oluşturun ve var olan NodeConfiguration 'ın üzerine yazılmaz.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="6b2ab-114">Bu komut, WebSunucusu. mof adındaki Otomasyon hesabına WebSunucusu. mof adlı dosyadan DSC</span><span class="sxs-lookup"><span data-stu-id="6b2ab-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="6b2ab-115">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6b2ab-116">ContosoConfiguration. webserver adlı bir DSC düğüm yapılandırması varsa, bu komut, Contosoyapılandırması [2]. webserver adlı yeni bir derleme sürümü ekler.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="6b2ab-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b2ab-117">PARAMETERS</span></span>

### <span data-ttu-id="6b2ab-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6b2ab-118">-AutomationAccountName</span></span>
<span data-ttu-id="6b2ab-119">Bu cmdlet 'in DSC düğüm yapılandırmasını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6b2ab-120">-ConfigurationName</span></span>
<span data-ttu-id="6b2ab-121">İçeri aktarılacak düğüm yapılandırmasının ad alanı ve kapsayıcısı olarak kullanılmak üzere bir DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2ab-122">-DefaultProfile</span></span>
<span data-ttu-id="6b2ab-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6b2ab-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6b2ab-124">-Force</span></span>
<span data-ttu-id="6b2ab-125">Bu cmdlet 'in Otomasyon 'daki mevcut bir DSC düğümü yapılandırmasını değiştirdiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-126">-Incrementnodeconfigurationbuıld</span><span class="sxs-lookup"><span data-stu-id="6b2ab-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="6b2ab-127">Yeni bir düğüm yapılandırması derleme sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="6b2ab-128">-Path</span></span>
<span data-ttu-id="6b2ab-129">Bu cmdlet 'in aldığı MOF yapılandırma belgesinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b2ab-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b2ab-131">Bu cmdlet 'in DSC düğüm yapılandırmasını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b2ab-132">-Confirm</span></span>
<span data-ttu-id="6b2ab-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2ab-134">-WhatIf</span></span>
<span data-ttu-id="6b2ab-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b2ab-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2ab-137">CommonParameters</span></span>
<span data-ttu-id="6b2ab-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2ab-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2ab-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2ab-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b2ab-140">INPUTS</span></span>

### <span data-ttu-id="6b2ab-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6b2ab-141">None</span></span>
<span data-ttu-id="6b2ab-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b2ab-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b2ab-143">OUTPUTS</span></span>

### <span data-ttu-id="6b2ab-144">Microsoft. Azure. Commands. Automation. model. Nodeyapılandırması</span><span class="sxs-lookup"><span data-stu-id="6b2ab-144">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="6b2ab-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b2ab-145">NOTES</span></span>

## <span data-ttu-id="6b2ab-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b2ab-146">RELATED LINKS</span></span>

[<span data-ttu-id="6b2ab-147">Dışarı aktarma-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b2ab-147">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="6b2ab-148">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b2ab-148">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


