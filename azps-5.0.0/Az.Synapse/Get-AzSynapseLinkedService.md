---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324193"
---
# <span data-ttu-id="6904a-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="6904a-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="6904a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6904a-102">SYNOPSIS</span></span>
<span data-ttu-id="6904a-103">Çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="6904a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6904a-104">SYNTAX</span></span>

### <span data-ttu-id="6904a-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6904a-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6904a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="6904a-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6904a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6904a-107">DESCRIPTION</span></span>
<span data-ttu-id="6904a-108">**Get-AzSynapseLinkedService** cmdlet 'i çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="6904a-109">Bağlantılı hizmetin adını belirtirseniz, bu cmdlet bu bağlantılı hizmet hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="6904a-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="6904a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6904a-111">EXAMPLES</span></span>

### <span data-ttu-id="6904a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6904a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6904a-113">Bu komut, ContosoWorkspace adlı çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6904a-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6904a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="6904a-115">Bu komut, ContosoWorkspace adındaki çalışma alanında ContosoLinkedService adındaki bağlantılı hizmetle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6904a-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6904a-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="6904a-117">Bu komut, ContosoLinkedService adındaki bağlantılı hizmetle ilgili olarak, ContosoWorkspace aracılığıyla Contosoçalışma alanında bulunan bir bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6904a-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6904a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6904a-118">PARAMETERS</span></span>

### <span data-ttu-id="6904a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6904a-119">-DefaultProfile</span></span>
<span data-ttu-id="6904a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6904a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6904a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6904a-121">-Name</span></span>
<span data-ttu-id="6904a-122">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="6904a-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6904a-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6904a-123">-WorkspaceName</span></span>
<span data-ttu-id="6904a-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="6904a-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6904a-125">-</span><span class="sxs-lookup"><span data-stu-id="6904a-125">-WorkspaceObject</span></span>
<span data-ttu-id="6904a-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="6904a-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6904a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6904a-127">CommonParameters</span></span>
<span data-ttu-id="6904a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6904a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6904a-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6904a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6904a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6904a-130">INPUTS</span></span>

### <span data-ttu-id="6904a-131">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6904a-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6904a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6904a-132">OUTPUTS</span></span>

### <span data-ttu-id="6904a-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="6904a-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="6904a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6904a-134">NOTES</span></span>

## <span data-ttu-id="6904a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6904a-135">RELATED LINKS</span></span>
