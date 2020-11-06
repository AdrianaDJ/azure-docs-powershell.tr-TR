---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591040"
---
# <span data-ttu-id="bed2d-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bed2d-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="bed2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bed2d-103">Kapsayıcı kayıt defteri için oturum açma kimlik bilgilerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bed2d-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bed2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bed2d-104">SYNTAX</span></span>

### <span data-ttu-id="bed2d-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bed2d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bed2d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bed2d-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bed2d-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bed2d-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bed2d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bed2d-108">DESCRIPTION</span></span>
<span data-ttu-id="bed2d-109">Update-AzureRmContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bed2d-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="bed2d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bed2d-110">EXAMPLES</span></span>

### <span data-ttu-id="bed2d-111">Örnek 1: kapsayıcı kayıt defteri için oturum açma kimlik bilgisini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="bed2d-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="bed2d-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bed2d-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="bed2d-113">Yönetici Kullanıcı, \` kayıt defteri myregistry 'nin \` oturum açma kimlik bilgilerini yeniden üretmelidir.</span><span class="sxs-lookup"><span data-stu-id="bed2d-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="bed2d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bed2d-114">PARAMETERS</span></span>

### <span data-ttu-id="bed2d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bed2d-115">-Name</span></span>
<span data-ttu-id="bed2d-116">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="bed2d-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed2d-117">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="bed2d-117">-PasswordName</span></span>
<span data-ttu-id="bed2d-118">Yeniden üretmek için parola adı.</span><span class="sxs-lookup"><span data-stu-id="bed2d-118">The name of password to regenerate.</span></span>
<span data-ttu-id="bed2d-119">İzin verilen değerler: parola, paSsWorD2.</span><span class="sxs-lookup"><span data-stu-id="bed2d-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed2d-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="bed2d-120">-Registry</span></span>
<span data-ttu-id="bed2d-121">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="bed2d-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bed2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bed2d-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bed2d-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed2d-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="bed2d-124">-Confirm</span></span>
<span data-ttu-id="bed2d-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bed2d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bed2d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bed2d-126">-WhatIf</span></span>
<span data-ttu-id="bed2d-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bed2d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bed2d-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bed2d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bed2d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed2d-129">-DefaultProfile</span></span>
<span data-ttu-id="bed2d-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bed2d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bed2d-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bed2d-131">-ResourceId</span></span>
<span data-ttu-id="bed2d-132">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bed2d-132">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bed2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed2d-133">CommonParameters</span></span>
<span data-ttu-id="bed2d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bed2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed2d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed2d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bed2d-136">INPUTS</span></span>

### <span data-ttu-id="bed2d-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bed2d-137">PSContainerRegistry</span></span>
<span data-ttu-id="bed2d-138">Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bed2d-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="bed2d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bed2d-139">OUTPUTS</span></span>

### <span data-ttu-id="bed2d-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bed2d-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="bed2d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bed2d-141">NOTES</span></span>

## <span data-ttu-id="bed2d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bed2d-142">RELATED LINKS</span></span>

[<span data-ttu-id="bed2d-143">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bed2d-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="bed2d-144">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bed2d-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="bed2d-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bed2d-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

