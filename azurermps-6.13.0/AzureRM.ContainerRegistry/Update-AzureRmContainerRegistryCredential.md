---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594425"
---
# <span data-ttu-id="82196-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="82196-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="82196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82196-102">SYNOPSIS</span></span>
<span data-ttu-id="82196-103">Kapsayıcı kayıt defteri için oturum açma kimlik bilgilerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82196-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82196-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82196-104">SYNTAX</span></span>

### <span data-ttu-id="82196-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="82196-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82196-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82196-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82196-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="82196-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82196-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="82196-108">DESCRIPTION</span></span>
<span data-ttu-id="82196-109">Update-AzureRmContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82196-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="82196-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82196-110">EXAMPLES</span></span>

### <span data-ttu-id="82196-111">Örnek 1: kapsayıcı kayıt defteri için oturum açma kimlik bilgisini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="82196-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="82196-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82196-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="82196-113">Yönetici Kullanıcı, \` kayıt defteri myregistry 'nin \` oturum açma kimlik bilgilerini yeniden üretmelidir.</span><span class="sxs-lookup"><span data-stu-id="82196-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="82196-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82196-114">PARAMETERS</span></span>

### <span data-ttu-id="82196-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82196-115">-DefaultProfile</span></span>
<span data-ttu-id="82196-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="82196-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82196-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="82196-117">-Name</span></span>
<span data-ttu-id="82196-118">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="82196-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82196-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="82196-119">-PasswordName</span></span>
<span data-ttu-id="82196-120">Yeniden üretmek için parola adı.</span><span class="sxs-lookup"><span data-stu-id="82196-120">The name of password to regenerate.</span></span>
<span data-ttu-id="82196-121">İzin verilen değerler: parola, paSsWorD2.</span><span class="sxs-lookup"><span data-stu-id="82196-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82196-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="82196-122">-Registry</span></span>
<span data-ttu-id="82196-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="82196-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82196-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82196-124">-ResourceGroupName</span></span>
<span data-ttu-id="82196-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="82196-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82196-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="82196-126">-ResourceId</span></span>
<span data-ttu-id="82196-127">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="82196-127">The container registry resource id</span></span>

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

### <span data-ttu-id="82196-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="82196-128">-Confirm</span></span>
<span data-ttu-id="82196-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82196-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82196-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82196-130">-WhatIf</span></span>
<span data-ttu-id="82196-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82196-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82196-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82196-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82196-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82196-133">CommonParameters</span></span>
<span data-ttu-id="82196-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82196-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82196-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82196-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82196-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82196-136">INPUTS</span></span>

### <span data-ttu-id="82196-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82196-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="82196-138">Parametreler: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82196-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="82196-139">System. String</span><span class="sxs-lookup"><span data-stu-id="82196-139">System.String</span></span>

## <span data-ttu-id="82196-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82196-140">OUTPUTS</span></span>

### <span data-ttu-id="82196-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="82196-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="82196-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82196-142">NOTES</span></span>

## <span data-ttu-id="82196-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82196-143">RELATED LINKS</span></span>

[<span data-ttu-id="82196-144">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82196-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="82196-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82196-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="82196-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="82196-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

