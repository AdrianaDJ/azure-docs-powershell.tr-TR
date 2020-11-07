---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 41f2e9c99c219ce34eee8ad4a0fde9b63616b7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916043"
---
# <span data-ttu-id="c1154-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c1154-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="c1154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1154-102">SYNOPSIS</span></span>
<span data-ttu-id="c1154-103">Tümleştirme hesabı derlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1154-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="c1154-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1154-104">SYNTAX</span></span>

### <span data-ttu-id="c1154-105">Byıntegrationaccountandfilepath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1154-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1154-106">Byıntegrationaccountandcontentlink</span><span class="sxs-lookup"><span data-stu-id="c1154-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1154-107">Byıntegrationaccountandfilebytes</span><span class="sxs-lookup"><span data-stu-id="c1154-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1154-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="c1154-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1154-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="c1154-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1154-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c1154-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1154-111">Byresourceıdandcontentlink</span><span class="sxs-lookup"><span data-stu-id="c1154-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1154-112">Byresourceıdandfilebytes</span><span class="sxs-lookup"><span data-stu-id="c1154-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1154-113">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="c1154-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1154-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1154-114">DESCRIPTION</span></span>
<span data-ttu-id="c1154-115">**Get-AzIntegrationAccountAssembly** cmdlet 'i bir tümleştirme hesabında yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1154-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="c1154-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1154-116">EXAMPLES</span></span>

### <span data-ttu-id="c1154-117">Örnek 1: yerel dosya kullanarak yeni derleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1154-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="c1154-118">"$LocalAssemblyFilePath" içinde yer alan dosya yolundaki yerel dosyayı kullanarak yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1154-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="c1154-119">Örnek 2: bayt verilerini kullanarak yeni derleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1154-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="c1154-120">"$AssemblyContent" içinde bulunan bir bayt dizisini kullanarak yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1154-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="c1154-121">Örnek 3: içerik bağlantısını kullanarak yeni derleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1154-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="c1154-122">"$AssemblyUrl" URL 'sinde bulunan bayt verilerini kullanarak yeni bir derleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1154-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="c1154-123">Büyük boyutlu derlemeler oluşturmak için önerilen yöntem budur.</span><span class="sxs-lookup"><span data-stu-id="c1154-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="c1154-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1154-124">PARAMETERS</span></span>

### <span data-ttu-id="c1154-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="c1154-125">-AssemblyData</span></span>
<span data-ttu-id="c1154-126">Tümleştirme hesabı derleme baytlık veriler.</span><span class="sxs-lookup"><span data-stu-id="c1154-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="c1154-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="c1154-127">-AssemblyFilePath</span></span>
<span data-ttu-id="c1154-128">Tümleştirme hesabı derleme dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="c1154-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="c1154-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="c1154-129">-ContentLink</span></span>
<span data-ttu-id="c1154-130">Tümleştirme hesabı derleme verilerine genel olarak erişilebilir bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="c1154-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="c1154-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1154-131">-DefaultProfile</span></span>
<span data-ttu-id="c1154-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1154-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1154-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c1154-133">-Metadata</span></span>
<span data-ttu-id="c1154-134">Tümleştirme hesabı derleme meta verileri.</span><span class="sxs-lookup"><span data-stu-id="c1154-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="c1154-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1154-135">-Name</span></span>
<span data-ttu-id="c1154-136">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="c1154-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="c1154-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="c1154-137">-ParentName</span></span>
<span data-ttu-id="c1154-138">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="c1154-138">The integration account name.</span></span>

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

### <span data-ttu-id="c1154-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1154-139">-ParentObject</span></span>
<span data-ttu-id="c1154-140">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c1154-140">An integration account object.</span></span>

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

### <span data-ttu-id="c1154-141">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="c1154-141">-ParentResourceId</span></span>
<span data-ttu-id="c1154-142">Tümleştirme hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c1154-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="c1154-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1154-143">-ResourceGroupName</span></span>
<span data-ttu-id="c1154-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c1154-144">The resource group name.</span></span>

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

### <span data-ttu-id="c1154-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1154-145">-Confirm</span></span>
<span data-ttu-id="c1154-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1154-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1154-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1154-147">-WhatIf</span></span>
<span data-ttu-id="c1154-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1154-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1154-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1154-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1154-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1154-150">CommonParameters</span></span>
<span data-ttu-id="c1154-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1154-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1154-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1154-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1154-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1154-153">INPUTS</span></span>

### <span data-ttu-id="c1154-154">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="c1154-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="c1154-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c1154-155">System.String</span></span>

## <span data-ttu-id="c1154-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1154-156">OUTPUTS</span></span>

### <span data-ttu-id="c1154-157">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c1154-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="c1154-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1154-158">NOTES</span></span>

## <span data-ttu-id="c1154-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1154-159">RELATED LINKS</span></span>
