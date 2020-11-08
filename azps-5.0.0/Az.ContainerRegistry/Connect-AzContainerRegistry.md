---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275590"
---
# <span data-ttu-id="1e14d-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e14d-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="1e14d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e14d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e14d-103">Azure kapsayıcısı kayıt defterinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1e14d-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="1e14d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e14d-104">SYNTAX</span></span>

### <span data-ttu-id="1e14d-105">WithoutNameAndPasswordParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e14d-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e14d-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e14d-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e14d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e14d-107">DESCRIPTION</span></span>
<span data-ttu-id="1e14d-108">Azure kapsayıcısı kayıt defterinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1e14d-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="1e14d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e14d-109">EXAMPLES</span></span>

### <span data-ttu-id="1e14d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e14d-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="1e14d-111">Azure hesabında oturum açarken kimlik bilgileri olmadan ACR oturumu açın.</span><span class="sxs-lookup"><span data-stu-id="1e14d-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="1e14d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e14d-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="1e14d-113">Yönetici Kullanıcı etkinleştirildiğinde Yönetici Kullanıcı adıyla ACR ile oturum açma.</span><span class="sxs-lookup"><span data-stu-id="1e14d-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="1e14d-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1e14d-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="1e14d-115">Hizmet sorumlusu uygulama KIMLIĞI ve parolasıyla oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1e14d-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="1e14d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e14d-116">PARAMETERS</span></span>

### <span data-ttu-id="1e14d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e14d-117">-DefaultProfile</span></span>
<span data-ttu-id="1e14d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e14d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e14d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e14d-119">-Name</span></span>
<span data-ttu-id="1e14d-120">Azure kapsayıcısı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="1e14d-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e14d-121">-Parola</span><span class="sxs-lookup"><span data-stu-id="1e14d-121">-Password</span></span>
<span data-ttu-id="1e14d-122">Azure kapsayıcısı kayıt defteri parolası.</span><span class="sxs-lookup"><span data-stu-id="1e14d-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e14d-123">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="1e14d-123">-UserName</span></span>
<span data-ttu-id="1e14d-124">Azure kapsayıcısı kayıt defteri Için Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1e14d-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e14d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e14d-125">CommonParameters</span></span>
<span data-ttu-id="1e14d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e14d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e14d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e14d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e14d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e14d-128">INPUTS</span></span>

### <span data-ttu-id="1e14d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1e14d-129">System.String</span></span>

## <span data-ttu-id="1e14d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e14d-130">OUTPUTS</span></span>

### <span data-ttu-id="1e14d-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e14d-131">System.Boolean</span></span>

## <span data-ttu-id="1e14d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e14d-132">NOTES</span></span>

## <span data-ttu-id="1e14d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e14d-133">RELATED LINKS</span></span>
