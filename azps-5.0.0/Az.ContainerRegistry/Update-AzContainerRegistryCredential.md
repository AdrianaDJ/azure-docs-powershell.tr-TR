---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321742"
---
# <span data-ttu-id="97351-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97351-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="97351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97351-102">SYNOPSIS</span></span>
<span data-ttu-id="97351-103">Kapsayıcı kayıt defteri için oturum açma kimlik bilgilerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97351-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="97351-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97351-104">SYNTAX</span></span>

### <span data-ttu-id="97351-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97351-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97351-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97351-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97351-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="97351-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97351-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97351-108">DESCRIPTION</span></span>
<span data-ttu-id="97351-109">Update-AzContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97351-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="97351-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97351-110">EXAMPLES</span></span>

### <span data-ttu-id="97351-111">Örnek 1: kapsayıcı kayıt defteri için oturum açma kimlik bilgisini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="97351-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="97351-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97351-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="97351-113">Yönetici Kullanıcı, \` kayıt defteri myregistry 'nin \` oturum açma kimlik bilgilerini yeniden üretmelidir.</span><span class="sxs-lookup"><span data-stu-id="97351-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="97351-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97351-114">PARAMETERS</span></span>

### <span data-ttu-id="97351-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97351-115">-DefaultProfile</span></span>
<span data-ttu-id="97351-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97351-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97351-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="97351-117">-Name</span></span>
<span data-ttu-id="97351-118">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="97351-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="97351-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="97351-119">-PasswordName</span></span>
<span data-ttu-id="97351-120">Yeniden üretmek için parola adı.</span><span class="sxs-lookup"><span data-stu-id="97351-120">The name of password to regenerate.</span></span>
<span data-ttu-id="97351-121">İzin verilen değerler: parola, paSsWorD2.</span><span class="sxs-lookup"><span data-stu-id="97351-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="97351-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="97351-122">-Registry</span></span>
<span data-ttu-id="97351-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="97351-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="97351-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97351-124">-ResourceGroupName</span></span>
<span data-ttu-id="97351-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="97351-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="97351-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97351-126">-ResourceId</span></span>
<span data-ttu-id="97351-127">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="97351-127">The container registry resource id</span></span>

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

### <span data-ttu-id="97351-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="97351-128">-Confirm</span></span>
<span data-ttu-id="97351-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97351-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97351-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97351-130">-WhatIf</span></span>
<span data-ttu-id="97351-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97351-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97351-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97351-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97351-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97351-133">CommonParameters</span></span>
<span data-ttu-id="97351-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97351-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97351-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97351-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97351-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97351-136">INPUTS</span></span>

### <span data-ttu-id="97351-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97351-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="97351-138">System. String</span><span class="sxs-lookup"><span data-stu-id="97351-138">System.String</span></span>

## <span data-ttu-id="97351-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97351-139">OUTPUTS</span></span>

### <span data-ttu-id="97351-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97351-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="97351-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97351-141">NOTES</span></span>

## <span data-ttu-id="97351-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97351-142">RELATED LINKS</span></span>

[<span data-ttu-id="97351-143">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97351-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="97351-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97351-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="97351-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97351-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

