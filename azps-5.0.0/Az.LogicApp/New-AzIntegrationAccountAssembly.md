---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278974"
---
# <span data-ttu-id="fcddd-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fcddd-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="fcddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcddd-102">SYNOPSIS</span></span>
<span data-ttu-id="fcddd-103">Tümleştirme hesabı derlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcddd-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="fcddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcddd-104">SYNTAX</span></span>

### <span data-ttu-id="fcddd-105">Byıntegrationaccountandfilepath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fcddd-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcddd-106">Byıntegrationaccountandcontentlink</span><span class="sxs-lookup"><span data-stu-id="fcddd-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcddd-107">Byıntegrationaccountandfilebytes</span><span class="sxs-lookup"><span data-stu-id="fcddd-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcddd-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="fcddd-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcddd-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="fcddd-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcddd-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fcddd-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcddd-111">Byresourceıdandcontentlink</span><span class="sxs-lookup"><span data-stu-id="fcddd-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcddd-112">Byresourceıdandfilebytes</span><span class="sxs-lookup"><span data-stu-id="fcddd-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcddd-113">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="fcddd-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcddd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcddd-114">DESCRIPTION</span></span>
<span data-ttu-id="fcddd-115">**Get-AzIntegrationAccountAssembly** cmdlet 'i bir tümleştirme hesabında yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcddd-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="fcddd-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcddd-116">EXAMPLES</span></span>

### <span data-ttu-id="fcddd-117">Örnek 1: yerel dosya kullanarak yeni derleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcddd-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="fcddd-118">"$LocalAssemblyFilePath" içinde yer alan dosya yolundaki yerel dosyayı kullanarak yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcddd-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="fcddd-119">Örnek 2: bayt verilerini kullanarak yeni derleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcddd-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="fcddd-120">"$AssemblyContent" içinde bulunan bir bayt dizisini kullanarak yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcddd-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="fcddd-121">Örnek 3: içerik bağlantısını kullanarak yeni derleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcddd-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="fcddd-122">"$AssemblyUrl" URL 'sinde bulunan bayt verilerini kullanarak yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcddd-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="fcddd-123">Büyük boyutlu derlemeler oluşturmak için önerilen yöntem budur.</span><span class="sxs-lookup"><span data-stu-id="fcddd-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="fcddd-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcddd-124">PARAMETERS</span></span>

### <span data-ttu-id="fcddd-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="fcddd-125">-AssemblyData</span></span>
<span data-ttu-id="fcddd-126">Tümleştirme hesabı derleme baytlık veriler.</span><span class="sxs-lookup"><span data-stu-id="fcddd-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="fcddd-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="fcddd-127">-AssemblyFilePath</span></span>
<span data-ttu-id="fcddd-128">Tümleştirme hesabı derleme dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="fcddd-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="fcddd-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="fcddd-129">-ContentLink</span></span>
<span data-ttu-id="fcddd-130">Tümleştirme hesabı derleme verilerine genel olarak erişilebilir bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="fcddd-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="fcddd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcddd-131">-DefaultProfile</span></span>
<span data-ttu-id="fcddd-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fcddd-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcddd-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fcddd-133">-Metadata</span></span>
<span data-ttu-id="fcddd-134">Tümleştirme hesabı derleme meta verileri.</span><span class="sxs-lookup"><span data-stu-id="fcddd-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="fcddd-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="fcddd-135">-Name</span></span>
<span data-ttu-id="fcddd-136">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="fcddd-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcddd-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="fcddd-137">-ParentName</span></span>
<span data-ttu-id="fcddd-138">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="fcddd-138">The integration account name.</span></span>

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

### <span data-ttu-id="fcddd-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fcddd-139">-ParentObject</span></span>
<span data-ttu-id="fcddd-140">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fcddd-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcddd-141">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="fcddd-141">-ParentResourceId</span></span>
<span data-ttu-id="fcddd-142">Tümleştirme hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fcddd-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="fcddd-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcddd-143">-ResourceGroupName</span></span>
<span data-ttu-id="fcddd-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fcddd-144">The resource group name.</span></span>

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

### <span data-ttu-id="fcddd-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="fcddd-145">-Confirm</span></span>
<span data-ttu-id="fcddd-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fcddd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcddd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcddd-147">-WhatIf</span></span>
<span data-ttu-id="fcddd-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcddd-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcddd-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fcddd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcddd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcddd-150">CommonParameters</span></span>
<span data-ttu-id="fcddd-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcddd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcddd-152">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcddd-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcddd-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcddd-153">INPUTS</span></span>

### <span data-ttu-id="fcddd-154">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="fcddd-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="fcddd-155">System. String</span><span class="sxs-lookup"><span data-stu-id="fcddd-155">System.String</span></span>

## <span data-ttu-id="fcddd-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcddd-156">OUTPUTS</span></span>

### <span data-ttu-id="fcddd-157">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fcddd-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="fcddd-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcddd-158">NOTES</span></span>

## <span data-ttu-id="fcddd-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcddd-159">RELATED LINKS</span></span>
