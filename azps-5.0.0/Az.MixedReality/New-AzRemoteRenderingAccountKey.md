---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277310"
---
# <span data-ttu-id="efdc1-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="efdc1-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="efdc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="efdc1-103">Uzaktan oluşturma hesabının anahtarı</span><span class="sxs-lookup"><span data-stu-id="efdc1-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="efdc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efdc1-104">SYNTAX</span></span>

### <span data-ttu-id="efdc1-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdc1-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdc1-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdc1-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdc1-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdc1-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdc1-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdc1-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdc1-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdc1-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdc1-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdc1-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efdc1-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="efdc1-111">DESCRIPTION</span></span>
<span data-ttu-id="efdc1-112">Uzak Işleme hesabının birincil anahtarını veya ikincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="efdc1-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="efdc1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efdc1-113">EXAMPLES</span></span>

### <span data-ttu-id="efdc1-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="efdc1-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="efdc1-115">"RG1" kaynak grubunda "örnek" uzaktan Işleme hesabının ikincil anahtarını yeniden üret.</span><span class="sxs-lookup"><span data-stu-id="efdc1-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="efdc1-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="efdc1-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="efdc1-117">Geçerli aboneliğin ve "RG1" kaynak grubundan yöneltme ile "örnek" uzaktan Işleme hesabı için ikincil anahtarı yeniden üret.</span><span class="sxs-lookup"><span data-stu-id="efdc1-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="efdc1-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efdc1-118">PARAMETERS</span></span>

### <span data-ttu-id="efdc1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdc1-119">-DefaultProfile</span></span>
<span data-ttu-id="efdc1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="efdc1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="efdc1-121">-Force</span></span>
<span data-ttu-id="efdc1-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="efdc1-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efdc1-123">-InputObject</span></span>
<span data-ttu-id="efdc1-124">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="efdc1-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="efdc1-125">-Name</span></span>
<span data-ttu-id="efdc1-126">Uzaktan Işleme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="efdc1-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-127">-Birincil</span><span class="sxs-lookup"><span data-stu-id="efdc1-127">-Primary</span></span>
<span data-ttu-id="efdc1-128">Uzaktan Işleme hesabının birincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="efdc1-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efdc1-129">-ResourceGroupName</span></span>
<span data-ttu-id="efdc1-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="efdc1-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="efdc1-131">-ResourceId</span></span>
<span data-ttu-id="efdc1-132">Uzaktan Işleme hesabı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="efdc1-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-133">-İkincil</span><span class="sxs-lookup"><span data-stu-id="efdc1-133">-Secondary</span></span>
<span data-ttu-id="efdc1-134">Uzaktan Işleme hesabının birincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="efdc1-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdc1-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="efdc1-135">-Confirm</span></span>
<span data-ttu-id="efdc1-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="efdc1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efdc1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efdc1-137">-WhatIf</span></span>
<span data-ttu-id="efdc1-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="efdc1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efdc1-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="efdc1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efdc1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdc1-140">CommonParameters</span></span>
<span data-ttu-id="efdc1-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efdc1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="efdc1-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efdc1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdc1-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efdc1-143">INPUTS</span></span>

### <span data-ttu-id="efdc1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="efdc1-144">System.String</span></span>

### <span data-ttu-id="efdc1-145">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="efdc1-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="efdc1-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efdc1-146">OUTPUTS</span></span>

### <span data-ttu-id="efdc1-147">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="efdc1-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="efdc1-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efdc1-148">NOTES</span></span>

## <span data-ttu-id="efdc1-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efdc1-149">RELATED LINKS</span></span>
