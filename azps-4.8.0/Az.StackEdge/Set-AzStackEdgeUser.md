---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268674"
---
# <span data-ttu-id="40fef-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="40fef-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="40fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40fef-102">SYNOPSIS</span></span>
<span data-ttu-id="40fef-103">Cihazda bir kullanıcı için yeni bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="40fef-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="40fef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40fef-104">SYNTAX</span></span>

### <span data-ttu-id="40fef-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40fef-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40fef-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="40fef-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40fef-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40fef-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40fef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="40fef-108">DESCRIPTION</span></span>
<span data-ttu-id="40fef-109">**Set-AzStackEdgeUser** cmdlet 'ı yığın uç cihazında bir kullanıcı için yeni bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="40fef-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="40fef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40fef-110">EXAMPLES</span></span>

### <span data-ttu-id="40fef-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="40fef-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="40fef-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40fef-112">PARAMETERS</span></span>

### <span data-ttu-id="40fef-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="40fef-113">-AsJob</span></span>
<span data-ttu-id="40fef-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="40fef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40fef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fef-115">-DefaultProfile</span></span>
<span data-ttu-id="40fef-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40fef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40fef-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="40fef-117">-DeviceName</span></span>
<span data-ttu-id="40fef-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="40fef-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-119">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="40fef-119">-EncryptionKey</span></span>
<span data-ttu-id="40fef-120">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="40fef-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40fef-121">-InputObject</span></span>
<span data-ttu-id="40fef-122">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="40fef-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="40fef-123">-Name</span></span>
<span data-ttu-id="40fef-124">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="40fef-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="40fef-125">-Password</span></span>
<span data-ttu-id="40fef-126">Parola, güvenli dize olarak sağla</span><span class="sxs-lookup"><span data-stu-id="40fef-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fef-127">-ResourceGroupName</span></span>
<span data-ttu-id="40fef-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="40fef-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="40fef-129">-ResourceId</span></span>
<span data-ttu-id="40fef-130">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="40fef-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fef-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="40fef-131">-Confirm</span></span>
<span data-ttu-id="40fef-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40fef-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40fef-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40fef-133">-WhatIf</span></span>
<span data-ttu-id="40fef-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40fef-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40fef-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40fef-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40fef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fef-136">CommonParameters</span></span>
<span data-ttu-id="40fef-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40fef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fef-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40fef-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fef-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40fef-139">INPUTS</span></span>

### <span data-ttu-id="40fef-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40fef-140">None</span></span>

## <span data-ttu-id="40fef-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40fef-141">OUTPUTS</span></span>

### <span data-ttu-id="40fef-142">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="40fef-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="40fef-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40fef-143">NOTES</span></span>

## <span data-ttu-id="40fef-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40fef-144">RELATED LINKS</span></span>
