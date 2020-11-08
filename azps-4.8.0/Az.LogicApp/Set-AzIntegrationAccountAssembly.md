---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267157"
---
# <span data-ttu-id="17387-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17387-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="17387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17387-102">SYNOPSIS</span></span>
<span data-ttu-id="17387-103">Tümleştirme hesabı derlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17387-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="17387-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17387-104">SYNTAX</span></span>

### <span data-ttu-id="17387-105">Byıntegrationaccountandfilepath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17387-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17387-106">Byıntegrationaccountandcontentlink</span><span class="sxs-lookup"><span data-stu-id="17387-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17387-107">Byıntegrationaccountandfilebytes</span><span class="sxs-lookup"><span data-stu-id="17387-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17387-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="17387-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17387-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="17387-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17387-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="17387-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17387-111">Byresourceıdandcontentlink</span><span class="sxs-lookup"><span data-stu-id="17387-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17387-112">Byresourceıdandfilebytes</span><span class="sxs-lookup"><span data-stu-id="17387-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17387-113">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="17387-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17387-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="17387-114">DESCRIPTION</span></span>
<span data-ttu-id="17387-115">**Set-AzIntegrationAccountAssembly** cmdlet 'i bir tümleştirme hesabı derlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17387-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="17387-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17387-116">EXAMPLES</span></span>

### <span data-ttu-id="17387-117">Örnek 1: yerel dosya kullanarak derlemeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="17387-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="17387-118">"SampleAssembly" adlı derlemeyi, "$localAssemblyFilePath" içindeki dosya yolundaki yerel dosyayı kullanarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17387-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="17387-119">Örnek 2: bayt verileri kullanarak derlemeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="17387-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="17387-120">"SampleAssembly" adlı derlemeyi, "$assemblyContent" içindeki bayt dizisini kullanarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17387-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="17387-121">Örnek 3: içerik bağlantısını kullanarak derlemeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="17387-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="17387-122">"$AssemblyUrl" URL 'sinde bulunan bayt verilerini kullanarak "sampleAssembly" adlı derlemeyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17387-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="17387-123">Büyük boyutlu derlemeler oluşturmak için önerilen yöntem budur.</span><span class="sxs-lookup"><span data-stu-id="17387-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="17387-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17387-124">PARAMETERS</span></span>

### <span data-ttu-id="17387-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="17387-125">-AssemblyData</span></span>
<span data-ttu-id="17387-126">Tümleştirme hesabı derleme baytlık veriler.</span><span class="sxs-lookup"><span data-stu-id="17387-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="17387-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="17387-127">-AssemblyFilePath</span></span>
<span data-ttu-id="17387-128">Tümleştirme hesabı derleme dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="17387-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="17387-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="17387-129">-ContentLink</span></span>
<span data-ttu-id="17387-130">Tümleştirme hesabı derleme verilerine genel olarak erişilebilir bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="17387-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="17387-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17387-131">-DefaultProfile</span></span>
<span data-ttu-id="17387-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17387-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17387-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17387-133">-InputObject</span></span>
<span data-ttu-id="17387-134">Tümleştirme hesabı derlemesi.</span><span class="sxs-lookup"><span data-stu-id="17387-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="17387-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="17387-135">-Metadata</span></span>
<span data-ttu-id="17387-136">Tümleştirme hesabı derleme meta verileri.</span><span class="sxs-lookup"><span data-stu-id="17387-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="17387-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="17387-137">-Name</span></span>
<span data-ttu-id="17387-138">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="17387-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="17387-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="17387-139">-ParentName</span></span>
<span data-ttu-id="17387-140">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="17387-140">The integration account name.</span></span>

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

### <span data-ttu-id="17387-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17387-141">-ResourceGroupName</span></span>
<span data-ttu-id="17387-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17387-142">The resource group name.</span></span>

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

### <span data-ttu-id="17387-143">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="17387-143">-ResourceId</span></span>
<span data-ttu-id="17387-144">Tümleştirme hesabı derleme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="17387-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="17387-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="17387-145">-Confirm</span></span>
<span data-ttu-id="17387-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17387-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17387-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17387-147">-WhatIf</span></span>
<span data-ttu-id="17387-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17387-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17387-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17387-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17387-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17387-150">CommonParameters</span></span>
<span data-ttu-id="17387-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17387-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17387-152">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17387-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17387-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17387-153">INPUTS</span></span>

### <span data-ttu-id="17387-154">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17387-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="17387-155">System. String</span><span class="sxs-lookup"><span data-stu-id="17387-155">System.String</span></span>

## <span data-ttu-id="17387-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17387-156">OUTPUTS</span></span>

### <span data-ttu-id="17387-157">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17387-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="17387-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17387-158">NOTES</span></span>

## <span data-ttu-id="17387-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17387-159">RELATED LINKS</span></span>
