---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319593"
---
# <span data-ttu-id="90e16-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90e16-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="90e16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e16-102">SYNOPSIS</span></span>
<span data-ttu-id="90e16-103">Kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90e16-103">Creates a container registry.</span></span>

## <span data-ttu-id="90e16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90e16-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90e16-105">DESCRIPTION</span></span>
<span data-ttu-id="90e16-106">New-AzContainerRegistry cmdlet 'i kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90e16-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="90e16-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90e16-107">EXAMPLES</span></span>

### <span data-ttu-id="90e16-108">Örnek 1: yeni bir depolama hesabıyla kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="90e16-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="90e16-109">Bu komut myresourcegroup kaynak grubunda yeni bir depolama hesabı içeren bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="90e16-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="90e16-110">Örnek 2: Yönetici Kullanıcı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="90e16-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="90e16-111">Bu komut Yönetici kullanıcısı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90e16-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="90e16-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90e16-112">PARAMETERS</span></span>

### <span data-ttu-id="90e16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e16-113">-DefaultProfile</span></span>
<span data-ttu-id="90e16-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="90e16-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90e16-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="90e16-115">-EnableAdminUser</span></span>
<span data-ttu-id="90e16-116">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="90e16-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="90e16-117">-Location</span></span>
<span data-ttu-id="90e16-118">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="90e16-118">Container Registry Location.</span></span>
<span data-ttu-id="90e16-119">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="90e16-119">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="90e16-120">-Name</span></span>
<span data-ttu-id="90e16-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="90e16-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e16-122">-ResourceGroupName</span></span>
<span data-ttu-id="90e16-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="90e16-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="90e16-124">-Sku</span></span>
<span data-ttu-id="90e16-125">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="90e16-125">Container Registry SKU.</span></span>
<span data-ttu-id="90e16-126">İzin verilen değerler: temel.</span><span class="sxs-lookup"><span data-stu-id="90e16-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="90e16-127">-Tag</span></span>
<span data-ttu-id="90e16-128">Kapsayıcı kayıt defteri etiketleri. karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="90e16-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="90e16-129">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="90e16-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="90e16-130">-Confirm</span></span>
<span data-ttu-id="90e16-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90e16-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e16-132">-WhatIf</span></span>
<span data-ttu-id="90e16-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90e16-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e16-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90e16-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e16-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e16-135">CommonParameters</span></span>
<span data-ttu-id="90e16-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90e16-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e16-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90e16-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e16-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90e16-138">INPUTS</span></span>

### <span data-ttu-id="90e16-139">System. String</span><span class="sxs-lookup"><span data-stu-id="90e16-139">System.String</span></span>

## <span data-ttu-id="90e16-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90e16-140">OUTPUTS</span></span>

### <span data-ttu-id="90e16-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90e16-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="90e16-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90e16-142">NOTES</span></span>

## <span data-ttu-id="90e16-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90e16-143">RELATED LINKS</span></span>

[<span data-ttu-id="90e16-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90e16-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="90e16-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90e16-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="90e16-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90e16-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

