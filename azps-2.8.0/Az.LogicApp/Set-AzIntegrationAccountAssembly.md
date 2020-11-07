---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a3f2c76de9dc331c6b073f724fede6a3bafeed18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751492"
---
# <span data-ttu-id="0d271-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0d271-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="0d271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d271-102">SYNOPSIS</span></span>
<span data-ttu-id="0d271-103">Tümleştirme hesabı derlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0d271-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="0d271-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d271-104">SYNTAX</span></span>

### <span data-ttu-id="0d271-105">Byıntegrationaccountandfilepath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d271-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d271-106">Byıntegrationaccountandcontentlink</span><span class="sxs-lookup"><span data-stu-id="0d271-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d271-107">Byıntegrationaccountandfilebytes</span><span class="sxs-lookup"><span data-stu-id="0d271-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d271-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="0d271-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d271-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="0d271-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d271-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="0d271-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d271-111">Byresourceıdandcontentlink</span><span class="sxs-lookup"><span data-stu-id="0d271-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d271-112">Byresourceıdandfilebytes</span><span class="sxs-lookup"><span data-stu-id="0d271-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d271-113">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="0d271-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d271-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d271-114">DESCRIPTION</span></span>
<span data-ttu-id="0d271-115">**Set-AzIntegrationAccountAssembly** cmdlet 'i bir tümleştirme hesabı derlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0d271-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="0d271-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d271-116">EXAMPLES</span></span>

### <span data-ttu-id="0d271-117">Örnek 1: yerel dosya kullanarak derlemeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="0d271-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="0d271-118">"SampleAssembly" adlı derlemeyi, "$localAssemblyFilePath" içindeki dosya yolundaki yerel dosyayı kullanarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0d271-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="0d271-119">Örnek 2: bayt verileri kullanarak derlemeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="0d271-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="0d271-120">"SampleAssembly" adlı derlemeyi, "$assemblyContent" içindeki bayt dizisini kullanarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0d271-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="0d271-121">Örnek 3: içerik bağlantısını kullanarak derlemeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="0d271-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="0d271-122">"$AssemblyUrl" URL 'sinde bulunan bayt verilerini kullanarak "sampleAssembly" adlı derlemeyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0d271-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="0d271-123">Büyük boyutlu derlemeler oluşturmak için önerilen yöntem budur.</span><span class="sxs-lookup"><span data-stu-id="0d271-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="0d271-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d271-124">PARAMETERS</span></span>

### <span data-ttu-id="0d271-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="0d271-125">-AssemblyData</span></span>
<span data-ttu-id="0d271-126">Tümleştirme hesabı derleme baytlık veriler.</span><span class="sxs-lookup"><span data-stu-id="0d271-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="0d271-127">-AssemblyFilePath</span></span>
<span data-ttu-id="0d271-128">Tümleştirme hesabı derleme dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="0d271-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="0d271-129">-ContentLink</span></span>
<span data-ttu-id="0d271-130">Tümleştirme hesabı derleme verilerine genel olarak erişilebilir bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="0d271-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d271-131">-DefaultProfile</span></span>
<span data-ttu-id="0d271-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d271-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d271-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d271-133">-InputObject</span></span>
<span data-ttu-id="0d271-134">Tümleştirme hesabı derlemesi.</span><span class="sxs-lookup"><span data-stu-id="0d271-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0d271-135">-Metadata</span></span>
<span data-ttu-id="0d271-136">Tümleştirme hesabı derleme meta verileri.</span><span class="sxs-lookup"><span data-stu-id="0d271-136">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d271-137">-Name</span></span>
<span data-ttu-id="0d271-138">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="0d271-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="0d271-139">-ParentName</span></span>
<span data-ttu-id="0d271-140">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="0d271-140">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d271-141">-ResourceGroupName</span></span>
<span data-ttu-id="0d271-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0d271-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-143">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0d271-143">-ResourceId</span></span>
<span data-ttu-id="0d271-144">Tümleştirme hesabı derleme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d271-144">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d271-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d271-145">-Confirm</span></span>
<span data-ttu-id="0d271-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d271-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d271-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d271-147">-WhatIf</span></span>
<span data-ttu-id="0d271-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d271-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d271-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d271-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d271-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d271-150">CommonParameters</span></span>
<span data-ttu-id="0d271-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d271-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d271-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d271-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d271-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d271-153">INPUTS</span></span>

### <span data-ttu-id="0d271-154">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0d271-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="0d271-155">System. String</span><span class="sxs-lookup"><span data-stu-id="0d271-155">System.String</span></span>

## <span data-ttu-id="0d271-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d271-156">OUTPUTS</span></span>

### <span data-ttu-id="0d271-157">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0d271-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="0d271-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d271-158">NOTES</span></span>

## <span data-ttu-id="0d271-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d271-159">RELATED LINKS</span></span>
