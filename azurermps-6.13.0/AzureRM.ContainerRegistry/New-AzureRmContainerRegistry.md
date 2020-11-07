---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: b70e4b4c184cfb6ebc5473cb0f49dec712bc62fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761976"
---
# <span data-ttu-id="4b819-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b819-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="4b819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b819-102">SYNOPSIS</span></span>
<span data-ttu-id="4b819-103">Kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b819-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b819-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b819-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b819-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b819-105">DESCRIPTION</span></span>
<span data-ttu-id="4b819-106">New-AzureRmContainerRegistry cmdlet 'i kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b819-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="4b819-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b819-107">EXAMPLES</span></span>

### <span data-ttu-id="4b819-108">Örnek 1: yeni bir depolama hesabıyla kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b819-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="4b819-109">Bu komut myresourcegroup kaynak grubunda yeni bir depolama hesabı içeren bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="4b819-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="4b819-110">Örnek 2: Yönetici Kullanıcı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b819-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="4b819-111">Bu komut Yönetici kullanıcısı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b819-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="4b819-112">Örnek 3: var olan bir depolama hesabıyla bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b819-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="4b819-113">Bu komut, aynı abonelikteki bir depolama hesabı mystorageaccount ile bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="4b819-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="4b819-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b819-114">PARAMETERS</span></span>

### <span data-ttu-id="4b819-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b819-115">-DefaultProfile</span></span>
<span data-ttu-id="4b819-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4b819-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b819-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="4b819-117">-EnableAdminUser</span></span>
<span data-ttu-id="4b819-118">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="4b819-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="4b819-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b819-119">-Location</span></span>
<span data-ttu-id="4b819-120">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="4b819-120">Container Registry Location.</span></span>
<span data-ttu-id="4b819-121">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="4b819-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="4b819-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b819-122">-Name</span></span>
<span data-ttu-id="4b819-123">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="4b819-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="4b819-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b819-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b819-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4b819-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4b819-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="4b819-126">-Sku</span></span>
<span data-ttu-id="4b819-127">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="4b819-127">Container Registry SKU.</span></span>
<span data-ttu-id="4b819-128">İzin verilen değerler: temel.</span><span class="sxs-lookup"><span data-stu-id="4b819-128">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="4b819-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4b819-129">-StorageAccountName</span></span>
<span data-ttu-id="4b819-130">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="4b819-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="4b819-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4b819-131">-Tag</span></span>
<span data-ttu-id="4b819-132">Kapsayıcı kayıt defteri etiketleri. karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4b819-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="4b819-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4b819-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4b819-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b819-134">-Confirm</span></span>
<span data-ttu-id="4b819-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b819-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b819-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b819-136">-WhatIf</span></span>
<span data-ttu-id="4b819-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b819-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b819-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b819-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b819-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b819-139">CommonParameters</span></span>
<span data-ttu-id="4b819-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b819-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b819-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b819-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b819-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b819-142">INPUTS</span></span>

### <span data-ttu-id="4b819-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4b819-143">System.String</span></span>

## <span data-ttu-id="4b819-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b819-144">OUTPUTS</span></span>

### <span data-ttu-id="4b819-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b819-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="4b819-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b819-146">NOTES</span></span>

## <span data-ttu-id="4b819-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b819-147">RELATED LINKS</span></span>

[<span data-ttu-id="4b819-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b819-148">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="4b819-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b819-149">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="4b819-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b819-150">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

