---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266462"
---
# <span data-ttu-id="29ec5-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="29ec5-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="29ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="29ec5-103">Dağıtım komut dosyalarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="29ec5-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="29ec5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29ec5-104">SYNTAX</span></span>

### <span data-ttu-id="29ec5-105">ListDeploymentScript (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29ec5-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29ec5-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="29ec5-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29ec5-107">Getdeploymentscriptbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="29ec5-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29ec5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="29ec5-108">DESCRIPTION</span></span>
<span data-ttu-id="29ec5-109">**Get-Azdeploymentscrıpt** cmdlet 'i tek bir dağıtım komut dosyası veya dağıtım komut dosyalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="29ec5-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="29ec5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29ec5-110">EXAMPLES</span></span>

### <span data-ttu-id="29ec5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29ec5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="29ec5-112">Geçerli kullanıcının bağlamında abonelikteki dağıtım komut dosyalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="29ec5-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="29ec5-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="29ec5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="29ec5-114">Kaynak grubundaki dağıtım komut dosyalarını listeler DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="29ec5-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="29ec5-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="29ec5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="29ec5-116">Kaynak Grup DS-TestRG 'daki Mydeploymentscrıpt adıyla bir dağıtım betiği alır.</span><span class="sxs-lookup"><span data-stu-id="29ec5-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="29ec5-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="29ec5-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="29ec5-118">Verilen kaynak kimliğiyle bir dağıtım betiği alır.</span><span class="sxs-lookup"><span data-stu-id="29ec5-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="29ec5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29ec5-119">PARAMETERS</span></span>

### <span data-ttu-id="29ec5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ec5-120">-DefaultProfile</span></span>
<span data-ttu-id="29ec5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29ec5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29ec5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="29ec5-122">-Id</span></span>
<span data-ttu-id="29ec5-123">Dağıtım komut dosyasının tam nitelikli kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="29ec5-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="29ec5-124">Örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="29ec5-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ec5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="29ec5-125">-Name</span></span>
<span data-ttu-id="29ec5-126">Dağıtım komut dosyasının adı</span><span class="sxs-lookup"><span data-stu-id="29ec5-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ec5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ec5-127">-ResourceGroupName</span></span>
<span data-ttu-id="29ec5-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29ec5-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ec5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ec5-129">CommonParameters</span></span>
<span data-ttu-id="29ec5-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29ec5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="29ec5-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ec5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ec5-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29ec5-132">INPUTS</span></span>

### <span data-ttu-id="29ec5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29ec5-133">System.String</span></span>

## <span data-ttu-id="29ec5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29ec5-134">OUTPUTS</span></span>

### <span data-ttu-id="29ec5-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="29ec5-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="29ec5-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29ec5-136">NOTES</span></span>

## <span data-ttu-id="29ec5-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29ec5-137">RELATED LINKS</span></span>
