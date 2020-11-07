---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 7a113bad74252778c32fc1273c9c3ca587bf1c2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752590"
---
# <span data-ttu-id="0bc89-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0bc89-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="0bc89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bc89-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc89-103">Kapsayıcı kayıt defteri için oturum açma kimlik bilgilerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bc89-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="0bc89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0bc89-104">SYNTAX</span></span>

### <span data-ttu-id="0bc89-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0bc89-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bc89-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc89-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc89-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0bc89-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc89-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0bc89-108">DESCRIPTION</span></span>
<span data-ttu-id="0bc89-109">Update-AzContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bc89-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="0bc89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0bc89-110">EXAMPLES</span></span>

### <span data-ttu-id="0bc89-111">Örnek 1: kapsayıcı kayıt defteri için oturum açma kimlik bilgisini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="0bc89-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="0bc89-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bc89-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="0bc89-113">Yönetici Kullanıcı, \` kayıt defteri myregistry 'nin \` oturum açma kimlik bilgilerini yeniden üretmelidir.</span><span class="sxs-lookup"><span data-stu-id="0bc89-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="0bc89-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0bc89-114">PARAMETERS</span></span>

### <span data-ttu-id="0bc89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc89-115">-DefaultProfile</span></span>
<span data-ttu-id="0bc89-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0bc89-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bc89-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0bc89-117">-Name</span></span>
<span data-ttu-id="0bc89-118">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="0bc89-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="0bc89-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="0bc89-119">-PasswordName</span></span>
<span data-ttu-id="0bc89-120">Yeniden üretmek için parola adı.</span><span class="sxs-lookup"><span data-stu-id="0bc89-120">The name of password to regenerate.</span></span>
<span data-ttu-id="0bc89-121">İzin verilen değerler: parola, paSsWorD2.</span><span class="sxs-lookup"><span data-stu-id="0bc89-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="0bc89-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="0bc89-122">-Registry</span></span>
<span data-ttu-id="0bc89-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0bc89-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="0bc89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc89-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bc89-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0bc89-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0bc89-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0bc89-126">-ResourceId</span></span>
<span data-ttu-id="0bc89-127">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0bc89-127">The container registry resource id</span></span>

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

### <span data-ttu-id="0bc89-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0bc89-128">-Confirm</span></span>
<span data-ttu-id="0bc89-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0bc89-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc89-130">-WhatIf</span></span>
<span data-ttu-id="0bc89-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0bc89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc89-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0bc89-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc89-133">CommonParameters</span></span>
<span data-ttu-id="0bc89-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0bc89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc89-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0bc89-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc89-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0bc89-136">INPUTS</span></span>

### <span data-ttu-id="0bc89-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0bc89-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="0bc89-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc89-138">System.String</span></span>

## <span data-ttu-id="0bc89-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0bc89-139">OUTPUTS</span></span>

### <span data-ttu-id="0bc89-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0bc89-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="0bc89-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0bc89-141">NOTES</span></span>

## <span data-ttu-id="0bc89-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0bc89-142">RELATED LINKS</span></span>

[<span data-ttu-id="0bc89-143">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0bc89-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="0bc89-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0bc89-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="0bc89-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0bc89-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

