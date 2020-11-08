---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274229"
---
# <span data-ttu-id="c5b6f-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c5b6f-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c5b6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b6f-103">Dağıtım betiği yürütme günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c5b6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5b6f-104">SYNTAX</span></span>

### <span data-ttu-id="c5b6f-105">GetDeploymentScriptLogByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5b6f-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5b6f-106">Getdeploymentscriptlogbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c5b6f-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5b6f-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5b6f-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5b6f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5b6f-108">DESCRIPTION</span></span>
<span data-ttu-id="c5b6f-109">**Get-AzDeploymentScriptLog** cmdlet 'i, dağıtım betiği yürütme günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c5b6f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5b6f-110">EXAMPLES</span></span>

### <span data-ttu-id="c5b6f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c5b6f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="c5b6f-112">Kaynak Grup DS-TestRG ' d a k i Mydeploymentscrıpt adlı bir dağıtım betiği günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c5b6f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c5b6f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="c5b6f-114">Kaynak grubu DS-TestRG ' d a k i Mydeploymentscrıpt adlı bir dağıtım betiği günlüğünün son 3 satırını alır.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c5b6f-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c5b6f-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="c5b6f-116">İlk komut, kaynak grubu DS-TestRG 'daki Mydeploymentscrıpt adıyla bir dağıtım betiği alır.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="c5b6f-117">İkinci komut, verilen dağıtım komut dosyasının günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="c5b6f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5b6f-118">PARAMETERS</span></span>

### <span data-ttu-id="c5b6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b6f-119">-DefaultProfile</span></span>
<span data-ttu-id="c5b6f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b6f-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="c5b6f-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="c5b6f-122">Dağıtım betiği PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b6f-123">-Deploymentscriptresourceıd</span><span class="sxs-lookup"><span data-stu-id="c5b6f-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c5b6f-124">Dağıtım komut dosyasının tam nitelikli kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c5b6f-125">Örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c5b6f-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b6f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5b6f-126">-Name</span></span>
<span data-ttu-id="c5b6f-127">Dağıtım komut dosyasının adı.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b6f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b6f-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5b6f-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b6f-130">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="c5b6f-130">-Tail</span></span>
<span data-ttu-id="c5b6f-131">Çıktıyı son n satırla sınırla</span><span class="sxs-lookup"><span data-stu-id="c5b6f-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b6f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b6f-132">CommonParameters</span></span>
<span data-ttu-id="c5b6f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b6f-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c5b6f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b6f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5b6f-135">INPUTS</span></span>

### <span data-ttu-id="c5b6f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c5b6f-136">System.String</span></span>

### <span data-ttu-id="c5b6f-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c5b6f-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="c5b6f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5b6f-138">OUTPUTS</span></span>

### <span data-ttu-id="c5b6f-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c5b6f-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="c5b6f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5b6f-140">NOTES</span></span>

## <span data-ttu-id="c5b6f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5b6f-141">RELATED LINKS</span></span>
