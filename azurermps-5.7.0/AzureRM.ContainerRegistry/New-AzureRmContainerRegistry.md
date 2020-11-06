---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587593"
---
# <span data-ttu-id="2fa60-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fa60-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="2fa60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa60-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa60-103">Kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fa60-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fa60-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa60-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fa60-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa60-106">New-AzureRmContainerRegistry cmdlet 'i kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fa60-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="2fa60-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fa60-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa60-108">Örnek 1: yeni bir depolama hesabıyla kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2fa60-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="2fa60-109">Bu komut myresourcegroup kaynak grubunda yeni bir depolama hesabı içeren bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="2fa60-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="2fa60-110">Örnek 2: Yönetici Kullanıcı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2fa60-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="2fa60-111">Bu komut Yönetici kullanıcısı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fa60-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="2fa60-112">Örnek 3: var olan bir depolama hesabıyla bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2fa60-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="2fa60-113">Bu komut, aynı abonelikteki bir depolama hesabı mystorageaccount ile bir kapsayıcı kayıt defteri oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="2fa60-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="2fa60-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fa60-114">PARAMETERS</span></span>

### <span data-ttu-id="2fa60-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="2fa60-115">-EnableAdminUser</span></span>
<span data-ttu-id="2fa60-116">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="2fa60-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="2fa60-117">-Location</span></span>
<span data-ttu-id="2fa60-118">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="2fa60-118">Container Registry Location.</span></span>
<span data-ttu-id="2fa60-119">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="2fa60-119">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fa60-120">-Name</span></span>
<span data-ttu-id="2fa60-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="2fa60-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa60-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fa60-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2fa60-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="2fa60-124">-Sku</span></span>
<span data-ttu-id="2fa60-125">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="2fa60-125">Container Registry SKU.</span></span>
<span data-ttu-id="2fa60-126">İzin verilen değerler: temel.</span><span class="sxs-lookup"><span data-stu-id="2fa60-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2fa60-127">-StorageAccountName</span></span>
<span data-ttu-id="2fa60-128">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="2fa60-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2fa60-129">-Tag</span></span>
<span data-ttu-id="2fa60-130">Kapsayıcı kayıt defteri etiketleri. karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2fa60-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="2fa60-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2fa60-131">For example:</span></span>

<span data-ttu-id="2fa60-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2fa60-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="2fa60-133">-Confirm</span></span>
<span data-ttu-id="2fa60-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2fa60-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa60-135">-WhatIf</span></span>
<span data-ttu-id="2fa60-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fa60-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa60-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2fa60-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa60-138">-DefaultProfile</span></span>
<span data-ttu-id="2fa60-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2fa60-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa60-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa60-140">CommonParameters</span></span>
<span data-ttu-id="2fa60-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fa60-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa60-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa60-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa60-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fa60-143">INPUTS</span></span>

### <span data-ttu-id="2fa60-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2fa60-144">None</span></span>
<span data-ttu-id="2fa60-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2fa60-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fa60-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fa60-146">OUTPUTS</span></span>

### <span data-ttu-id="2fa60-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fa60-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="2fa60-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fa60-148">NOTES</span></span>

## <span data-ttu-id="2fa60-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fa60-149">RELATED LINKS</span></span>

[<span data-ttu-id="2fa60-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fa60-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="2fa60-151">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fa60-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="2fa60-152">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fa60-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

