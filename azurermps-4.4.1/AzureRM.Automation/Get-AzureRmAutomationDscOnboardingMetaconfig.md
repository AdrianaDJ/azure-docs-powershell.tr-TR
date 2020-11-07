---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 58d15476921005b6da674d6a16441eb2e4f82865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591200"
---
# <span data-ttu-id="cd487-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="cd487-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="cd487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd487-102">SYNOPSIS</span></span>
<span data-ttu-id="cd487-103">Meta-Configuration. mof dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-103">Creates meta-configuration .mof files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd487-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd487-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd487-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd487-105">DESCRIPTION</span></span>
<span data-ttu-id="cd487-106">**Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet 'ı, APS Istenen durum yapılandırma (DSC) meta yapılandırma yönetilen nesne BIÇIMI (MOF) dosyalarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-106">The **Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="cd487-107">Bu cmdlet, belirttiğiniz her bilgisayar adına bir. mof dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="cd487-108">Cmdlet. mof dosyaları için bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="cd487-109">Bu bilgisayarlar için Set-DscLocalConfigurationManager cmdlet 'ini bir Azure Otomasyonu hesabında DSC düğümleri olarak eklemek için çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd487-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="cd487-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd487-110">EXAMPLES</span></span>

### <span data-ttu-id="cd487-111">Örnek 1: tüm sunucuları Automation DSC 'ye ekleme</span><span class="sxs-lookup"><span data-stu-id="cd487-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="cd487-112">İlk komut, Contoso17 adlı Otomasyon hesabı için iki sunucu için DSC meta yapılandırma dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="cd487-113">Komut bu dosyaları bir masaüstüne kaydeder.</span><span class="sxs-lookup"><span data-stu-id="cd487-113">The command saves these files on a desktop.</span></span>

<span data-ttu-id="cd487-114">İkinci komut, **set-DscLocalConfigurationManager** cmdlet 'ini kullanarak, meta yapılandırmasını DSC düğümleri olarak eklemek üzere belirtilen bilgisayarlara uygular.</span><span class="sxs-lookup"><span data-stu-id="cd487-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="cd487-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd487-115">PARAMETERS</span></span>

### <span data-ttu-id="cd487-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd487-116">-AutomationAccountName</span></span>
<span data-ttu-id="cd487-117">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd487-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="cd487-118">*ComputerName* parametresinin belirttiği bilgisayarları bu parametrenin belirttiği hesaba ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd487-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd487-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="cd487-119">-ComputerName</span></span>
<span data-ttu-id="cd487-120">Bu cmdlet. MOF dosyalarını oluşturan bilgisayarların adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd487-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="cd487-121">Bu parametreyi belirtmezseniz, cmdlet geçerli bilgisayar (localhost) için bir. mof dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="cd487-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cd487-122">-Force</span></span>
<span data-ttu-id="cd487-123">Komutu onay istemeden çalışmaya zorlar ve aynı ada sahip mevcut. MOF dosyalarını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd487-123">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="cd487-124">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="cd487-124">-OutputFolder</span></span>
<span data-ttu-id="cd487-125">Bu cmdlet. MOF dosyalarını depolayan bir klasörün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd487-125">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="cd487-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd487-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd487-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd487-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cd487-128">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bilgisayarlara. mof dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd487-128">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd487-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd487-129">-Confirm</span></span>
<span data-ttu-id="cd487-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd487-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd487-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd487-131">-WhatIf</span></span>
<span data-ttu-id="cd487-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd487-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd487-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd487-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd487-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd487-134">-DefaultProfile</span></span>
<span data-ttu-id="cd487-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd487-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd487-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd487-136">CommonParameters</span></span>
<span data-ttu-id="cd487-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd487-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd487-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd487-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd487-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd487-139">INPUTS</span></span>

## <span data-ttu-id="cd487-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd487-140">OUTPUTS</span></span>

### <span data-ttu-id="cd487-141">Microsoft. Azure. Commands. Automation. model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="cd487-141">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="cd487-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd487-142">NOTES</span></span>

## <span data-ttu-id="cd487-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd487-143">RELATED LINKS</span></span>
