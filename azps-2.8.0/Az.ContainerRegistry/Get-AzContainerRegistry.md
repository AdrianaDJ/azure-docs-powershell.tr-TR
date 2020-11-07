---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: f833d2f46c67964356f48a06c35d41dfcf090fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752613"
---
# <span data-ttu-id="9d779-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d779-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="9d779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d779-102">SYNOPSIS</span></span>
<span data-ttu-id="9d779-103">Kapsayıcı bir kayıt defteri alır.</span><span class="sxs-lookup"><span data-stu-id="9d779-103">Gets a container registry.</span></span>

## <span data-ttu-id="9d779-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d779-104">SYNTAX</span></span>

### <span data-ttu-id="9d779-105">Listkayıt Triesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9d779-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d779-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d779-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d779-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9d779-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d779-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d779-108">DESCRIPTION</span></span>
<span data-ttu-id="9d779-109">Get-AzContainerRegistry cmdlet 'i, bir kaynak grubundaki veya abonelikteki tüm kapsayıcı kayıt defterini veya tüm kapsayıcı kayıt defterleri 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="9d779-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="9d779-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d779-110">EXAMPLES</span></span>

### <span data-ttu-id="9d779-111">Örnek 1: belirtilen kapsayıcı kayıt defterini alma</span><span class="sxs-lookup"><span data-stu-id="9d779-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="9d779-112">Bu komut belirtilen kapsayıcı kayıt defterini alır.</span><span class="sxs-lookup"><span data-stu-id="9d779-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="9d779-113">Örnek 2: kaynak grubundaki tüm kapsayıcı kayıt defterlerine ulaşın</span><span class="sxs-lookup"><span data-stu-id="9d779-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="9d779-114">Bu komut, kaynak grubundaki tüm kapsayıcı kayıt defterleri 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="9d779-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="9d779-115">Örnek 3: abonelikteki tüm kapsayıcı kayıt defterlerine ulaşın</span><span class="sxs-lookup"><span data-stu-id="9d779-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="9d779-116">Bu komut, abonelikteki tüm kapsayıcı kayıt defterlerine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="9d779-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="9d779-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d779-117">PARAMETERS</span></span>

### <span data-ttu-id="9d779-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d779-118">-DefaultProfile</span></span>
<span data-ttu-id="9d779-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9d779-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d779-120">-Includedetail</span><span class="sxs-lookup"><span data-stu-id="9d779-120">-IncludeDetail</span></span>
<span data-ttu-id="9d779-121">Kapsayıcı kayıt defteri hakkında daha fazla bilgi göster.</span><span class="sxs-lookup"><span data-stu-id="9d779-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="9d779-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d779-122">-Name</span></span>
<span data-ttu-id="9d779-123">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="9d779-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d779-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d779-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d779-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9d779-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d779-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9d779-126">-ResourceId</span></span>
<span data-ttu-id="9d779-127">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9d779-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d779-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d779-128">CommonParameters</span></span>
<span data-ttu-id="9d779-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d779-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d779-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9d779-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d779-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d779-131">INPUTS</span></span>

### <span data-ttu-id="9d779-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9d779-132">System.String</span></span>

## <span data-ttu-id="9d779-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d779-133">OUTPUTS</span></span>

### <span data-ttu-id="9d779-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d779-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="9d779-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d779-135">NOTES</span></span>

## <span data-ttu-id="9d779-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d779-136">RELATED LINKS</span></span>

[<span data-ttu-id="9d779-137">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d779-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="9d779-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d779-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="9d779-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d779-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)
