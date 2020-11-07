---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 6598f2f990567301a3604327a213696f4cc825dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752604"
---
# <span data-ttu-id="c8b55-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8b55-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="c8b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b55-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b55-103">Kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8b55-103">Creates a container registry.</span></span>

## <span data-ttu-id="c8b55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8b55-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8b55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8b55-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b55-106">New-AzContainerRegistry cmdlet 'i kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8b55-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c8b55-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8b55-107">EXAMPLES</span></span>

### <span data-ttu-id="c8b55-108">Örnek 1: yeni bir depolama hesabıyla kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c8b55-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c8b55-109">Bu komut myresourcegroup kaynak grubunda yeni bir depolama hesabı içeren bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="c8b55-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="c8b55-110">Örnek 2: Yönetici Kullanıcı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c8b55-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c8b55-111">Bu komut Yönetici kullanıcısı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8b55-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="c8b55-112">Örnek 3: var olan bir depolama hesabıyla bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c8b55-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c8b55-113">Bu komut, aynı abonelikteki bir depolama hesabı mystorageaccount ile bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="c8b55-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="c8b55-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8b55-114">PARAMETERS</span></span>

### <span data-ttu-id="c8b55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b55-115">-DefaultProfile</span></span>
<span data-ttu-id="c8b55-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8b55-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8b55-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c8b55-117">-EnableAdminUser</span></span>
<span data-ttu-id="c8b55-118">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="c8b55-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="c8b55-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="c8b55-119">-Location</span></span>
<span data-ttu-id="c8b55-120">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="c8b55-120">Container Registry Location.</span></span>
<span data-ttu-id="c8b55-121">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="c8b55-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c8b55-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8b55-122">-Name</span></span>
<span data-ttu-id="c8b55-123">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="c8b55-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="c8b55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8b55-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8b55-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c8b55-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8b55-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c8b55-126">-Sku</span></span>
<span data-ttu-id="c8b55-127">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="c8b55-127">Container Registry SKU.</span></span>
<span data-ttu-id="c8b55-128">İzin verilen değerler: temel.</span><span class="sxs-lookup"><span data-stu-id="c8b55-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b55-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8b55-129">-StorageAccountName</span></span>
<span data-ttu-id="c8b55-130">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="c8b55-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="c8b55-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c8b55-131">-Tag</span></span>
<span data-ttu-id="c8b55-132">Kapsayıcı kayıt defteri etiketleri. karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c8b55-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="c8b55-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c8b55-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8b55-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="c8b55-134">-Confirm</span></span>
<span data-ttu-id="c8b55-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c8b55-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8b55-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8b55-136">-WhatIf</span></span>
<span data-ttu-id="c8b55-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8b55-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8b55-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c8b55-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8b55-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b55-139">CommonParameters</span></span>
<span data-ttu-id="c8b55-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8b55-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b55-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c8b55-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b55-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8b55-142">INPUTS</span></span>

### <span data-ttu-id="c8b55-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c8b55-143">System.String</span></span>

## <span data-ttu-id="c8b55-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8b55-144">OUTPUTS</span></span>

### <span data-ttu-id="c8b55-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8b55-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c8b55-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8b55-146">NOTES</span></span>

## <span data-ttu-id="c8b55-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8b55-147">RELATED LINKS</span></span>

[<span data-ttu-id="c8b55-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8b55-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="c8b55-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8b55-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="c8b55-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8b55-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

