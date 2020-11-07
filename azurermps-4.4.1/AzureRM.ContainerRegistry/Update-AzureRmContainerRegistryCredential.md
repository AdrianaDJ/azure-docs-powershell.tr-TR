---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762707"
---
# <span data-ttu-id="c7dea-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c7dea-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="c7dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7dea-102">SYNOPSIS</span></span>
<span data-ttu-id="c7dea-103">Kapsayıcı kayıt defteri için oturum açma kimlik bilgilerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7dea-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7dea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7dea-104">SYNTAX</span></span>

### <span data-ttu-id="c7dea-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7dea-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7dea-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7dea-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7dea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7dea-107">DESCRIPTION</span></span>
<span data-ttu-id="c7dea-108">**Update-AzureRmContainerRegistryCredential** cmdlet 'i, kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7dea-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="c7dea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7dea-109">EXAMPLES</span></span>

### <span data-ttu-id="c7dea-110">Örnek 1: kapsayıcı kayıt defteri için oturum açma kimlik bilgisini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7dea-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="c7dea-111">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7dea-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="c7dea-112">`MyRegistry`Oturum açma kimlik bilgilerini yeniden oluşturması için Yönetici Kullanıcı kapsayıcı kayıt defteri için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c7dea-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="c7dea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7dea-113">PARAMETERS</span></span>

### <span data-ttu-id="c7dea-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7dea-114">-Name</span></span>
<span data-ttu-id="c7dea-115">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="c7dea-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="c7dea-116">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="c7dea-116">-PasswordName</span></span>
<span data-ttu-id="c7dea-117">Yeniden üretmek için parola adı.</span><span class="sxs-lookup"><span data-stu-id="c7dea-117">The name of password to regenerate.</span></span>
<span data-ttu-id="c7dea-118">İzin verilen değerler: parola, paSsWorD2.</span><span class="sxs-lookup"><span data-stu-id="c7dea-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dea-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="c7dea-119">-Registry</span></span>
<span data-ttu-id="c7dea-120">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c7dea-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="c7dea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7dea-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7dea-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c7dea-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7dea-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7dea-123">-Confirm</span></span>
<span data-ttu-id="c7dea-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7dea-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7dea-125">-WhatIf</span></span>
<span data-ttu-id="c7dea-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7dea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7dea-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7dea-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dea-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7dea-128">-DefaultProfile</span></span>
<span data-ttu-id="c7dea-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7dea-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7dea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7dea-130">CommonParameters</span></span>
<span data-ttu-id="c7dea-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7dea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7dea-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7dea-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7dea-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7dea-133">INPUTS</span></span>

### <span data-ttu-id="c7dea-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7dea-134">PSContainerRegistry</span></span>
<span data-ttu-id="c7dea-135">Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c7dea-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="c7dea-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7dea-136">OUTPUTS</span></span>

### <span data-ttu-id="c7dea-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c7dea-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="c7dea-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7dea-138">NOTES</span></span>

## <span data-ttu-id="c7dea-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7dea-139">RELATED LINKS</span></span>

[<span data-ttu-id="c7dea-140">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7dea-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="c7dea-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7dea-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c7dea-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c7dea-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

