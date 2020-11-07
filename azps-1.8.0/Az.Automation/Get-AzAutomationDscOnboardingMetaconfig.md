---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 0302803568bac71baed28615552848f113da32df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761620"
---
# <span data-ttu-id="91653-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="91653-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="91653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91653-102">SYNOPSIS</span></span>
<span data-ttu-id="91653-103">Meta-Configuration. mof dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="91653-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91653-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91653-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91653-105">DESCRIPTION</span></span>
<span data-ttu-id="91653-106">**Get-AzAutomationDscOnboardingMetaconfig** cmdlet 'ı, APS Istenen durum yapılandırma (DSC) meta yapılandırma yönetilen nesne BIÇIMI (MOF) dosyalarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="91653-107">Bu cmdlet, belirttiğiniz her bilgisayar adına bir. mof dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="91653-108">Cmdlet. mof dosyaları için bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="91653-109">Bu bilgisayarlar için Set-DscLocalConfigurationManager cmdlet 'ini bir Azure Otomasyonu hesabında DSC düğümleri olarak eklemek için çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91653-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="91653-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91653-110">EXAMPLES</span></span>

### <span data-ttu-id="91653-111">Örnek 1: tüm sunucuları Automation DSC 'ye ekleme</span><span class="sxs-lookup"><span data-stu-id="91653-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="91653-112">İlk komut, Contoso17 adlı Otomasyon hesabı için iki sunucu için DSC meta yapılandırma dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="91653-113">Komut bu dosyaları bir masaüstüne kaydeder.</span><span class="sxs-lookup"><span data-stu-id="91653-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="91653-114">İkinci komut, **set-DscLocalConfigurationManager** cmdlet 'ini kullanarak, meta yapılandırmasını DSC düğümleri olarak eklemek üzere belirtilen bilgisayarlara uygular.</span><span class="sxs-lookup"><span data-stu-id="91653-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="91653-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91653-115">PARAMETERS</span></span>

### <span data-ttu-id="91653-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="91653-116">-AutomationAccountName</span></span>
<span data-ttu-id="91653-117">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91653-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="91653-118">*ComputerName* parametresinin belirttiği bilgisayarları bu parametrenin belirttiği hesaba ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91653-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="91653-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="91653-119">-ComputerName</span></span>
<span data-ttu-id="91653-120">Bu cmdlet. MOF dosyalarını oluşturan bilgisayarların adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91653-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="91653-121">Bu parametreyi belirtmezseniz, cmdlet geçerli bilgisayar (localhost) için bir. mof dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91653-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91653-122">-DefaultProfile</span></span>
<span data-ttu-id="91653-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="91653-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91653-124">-Force</span><span class="sxs-lookup"><span data-stu-id="91653-124">-Force</span></span>
<span data-ttu-id="91653-125">Komutu onay istemeden çalışmaya zorlar ve aynı ada sahip mevcut. MOF dosyalarını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91653-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="91653-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="91653-126">-OutputFolder</span></span>
<span data-ttu-id="91653-127">Bu cmdlet. MOF dosyalarını depolayan bir klasörün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91653-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91653-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91653-128">-ResourceGroupName</span></span>
<span data-ttu-id="91653-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91653-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="91653-130">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bilgisayarlara. mof dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91653-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="91653-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="91653-131">-Confirm</span></span>
<span data-ttu-id="91653-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91653-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91653-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91653-133">-WhatIf</span></span>
<span data-ttu-id="91653-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91653-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91653-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91653-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91653-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91653-136">CommonParameters</span></span>
<span data-ttu-id="91653-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91653-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91653-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91653-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91653-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91653-139">INPUTS</span></span>

### <span data-ttu-id="91653-140">System. String</span><span class="sxs-lookup"><span data-stu-id="91653-140">System.String</span></span>

### <span data-ttu-id="91653-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="91653-141">System.String[]</span></span>

## <span data-ttu-id="91653-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91653-142">OUTPUTS</span></span>

### <span data-ttu-id="91653-143">Microsoft. Azure. Commands. Automation. model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="91653-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="91653-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91653-144">NOTES</span></span>

## <span data-ttu-id="91653-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91653-145">RELATED LINKS</span></span>
