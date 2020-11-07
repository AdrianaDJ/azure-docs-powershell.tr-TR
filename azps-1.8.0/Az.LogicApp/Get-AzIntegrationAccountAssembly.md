---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: e854d9e77ba72ca297b2b9ca9a8d20f55d6194fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916116"
---
# <span data-ttu-id="d7bc2-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7bc2-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d7bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bc2-103">Tümleştirme hesabı derlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="d7bc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7bc2-104">SYNTAX</span></span>

### <span data-ttu-id="d7bc2-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7bc2-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bc2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7bc2-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bc2-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d7bc2-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7bc2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7bc2-108">DESCRIPTION</span></span>
<span data-ttu-id="d7bc2-109">**Get-AzIntegrationAccountAssembly** cmdlet 'i bir tümleştirme hesabından derleme alır.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="d7bc2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7bc2-110">EXAMPLES</span></span>

### <span data-ttu-id="d7bc2-111">Örnek 1: parametrelerle derleme alma</span><span class="sxs-lookup"><span data-stu-id="d7bc2-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d7bc2-112">"Sampleleresourcegroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleAssembly" adlı bir derleme alın.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="d7bc2-113">Örnek 2: parametrelere göre tümleştirme hesabındaki tüm derlemeleri listeleme</span><span class="sxs-lookup"><span data-stu-id="d7bc2-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d7bc2-114">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabındaki tüm birleştirmeleri edinin.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="d7bc2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7bc2-115">PARAMETERS</span></span>

### <span data-ttu-id="d7bc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bc2-116">-DefaultProfile</span></span>
<span data-ttu-id="d7bc2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7bc2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7bc2-118">-Name</span></span>
<span data-ttu-id="d7bc2-119">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc2-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d7bc2-120">-ParentName</span></span>
<span data-ttu-id="d7bc2-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7bc2-122">-ParentObject</span></span>
<span data-ttu-id="d7bc2-123">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc2-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="d7bc2-124">-ParentResourceId</span></span>
<span data-ttu-id="d7bc2-125">Tümleştirme hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7bc2-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bc2-128">CommonParameters</span></span>
<span data-ttu-id="d7bc2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7bc2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bc2-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bc2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bc2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7bc2-131">INPUTS</span></span>

### <span data-ttu-id="d7bc2-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="d7bc2-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d7bc2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d7bc2-133">System.String</span></span>

## <span data-ttu-id="d7bc2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7bc2-134">OUTPUTS</span></span>

### <span data-ttu-id="d7bc2-135">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7bc2-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d7bc2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7bc2-136">NOTES</span></span>

## <span data-ttu-id="d7bc2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7bc2-137">RELATED LINKS</span></span>
