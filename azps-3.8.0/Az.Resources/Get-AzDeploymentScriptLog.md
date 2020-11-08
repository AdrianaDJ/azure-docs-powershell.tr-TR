---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104319"
---
# <span data-ttu-id="f5c9c-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f5c9c-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="f5c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c9c-103">Dağıtım betiği yürütme günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f5c9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5c9c-104">SYNTAX</span></span>

### <span data-ttu-id="f5c9c-105">GetDeploymentScriptLogByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5c9c-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c9c-106">Getdeploymentscriptlogbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5c9c-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5c9c-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5c9c-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c9c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5c9c-108">DESCRIPTION</span></span>
<span data-ttu-id="f5c9c-109">**Get-AzDeploymentScriptLog** cmdlet 'i, dağıtım betiği yürütme günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f5c9c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5c9c-110">EXAMPLES</span></span>

### <span data-ttu-id="f5c9c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5c9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f5c9c-112">Kaynak Grup DS-TestRG 'daki Mydeploymentscrıpt adlı bir dağıtım komut dosyasının günlüklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f5c9c-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f5c9c-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="f5c9c-114">İlk komut, kaynak grubu DS-TestRG 'daki Mydeploymentscrıpt adıyla bir dağıtım betiği alır.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="f5c9c-115">İkinci komut, verilen dağıtım komut dosyasının günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="f5c9c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5c9c-116">PARAMETERS</span></span>

### <span data-ttu-id="f5c9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c9c-117">-DefaultProfile</span></span>
<span data-ttu-id="f5c9c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c9c-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="f5c9c-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="f5c9c-120">Dağıtım betiği PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c9c-121">-Deploymentscriptresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5c9c-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="f5c9c-122">Dağıtım komut dosyasının tam nitelikli kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f5c9c-123">Örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f5c9c-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c9c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5c9c-124">-Name</span></span>
<span data-ttu-id="f5c9c-125">Dağıtım komut dosyasının adı.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5c9c-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c9c-128">CommonParameters</span></span>
<span data-ttu-id="f5c9c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5c9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f5c9c-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c9c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c9c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5c9c-131">INPUTS</span></span>

### <span data-ttu-id="f5c9c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f5c9c-132">System.String</span></span>

### <span data-ttu-id="f5c9c-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f5c9c-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f5c9c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5c9c-134">OUTPUTS</span></span>

### <span data-ttu-id="f5c9c-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f5c9c-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="f5c9c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5c9c-136">NOTES</span></span>

## <span data-ttu-id="f5c9c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5c9c-137">RELATED LINKS</span></span>
