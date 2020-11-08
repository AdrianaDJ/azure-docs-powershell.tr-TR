---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097550"
---
# <span data-ttu-id="69250-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="69250-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="69250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69250-102">SYNOPSIS</span></span>
<span data-ttu-id="69250-103">Cihazda bir kullanıcı için yeni bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="69250-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="69250-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69250-104">SYNTAX</span></span>

### <span data-ttu-id="69250-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69250-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69250-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="69250-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69250-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69250-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69250-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="69250-108">DESCRIPTION</span></span>
<span data-ttu-id="69250-109">**Set-AzDataBoxEdgeUser** cmdlet 'ı, veri kutusu Edge cihazında bir kullanıcı için yeni bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="69250-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="69250-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69250-110">EXAMPLES</span></span>

### <span data-ttu-id="69250-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="69250-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="69250-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69250-112">PARAMETERS</span></span>

### <span data-ttu-id="69250-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="69250-113">-AsJob</span></span>
<span data-ttu-id="69250-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="69250-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69250-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69250-115">-DefaultProfile</span></span>
<span data-ttu-id="69250-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69250-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69250-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="69250-117">-DeviceName</span></span>
<span data-ttu-id="69250-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="69250-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69250-119">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="69250-119">-EncryptionKey</span></span>
<span data-ttu-id="69250-120">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="69250-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="69250-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69250-121">-InputObject</span></span>
<span data-ttu-id="69250-122">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="69250-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69250-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="69250-123">-Name</span></span>
<span data-ttu-id="69250-124">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="69250-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69250-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="69250-125">-Password</span></span>
<span data-ttu-id="69250-126">Parola, güvenli dize olarak sağla</span><span class="sxs-lookup"><span data-stu-id="69250-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="69250-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69250-127">-ResourceGroupName</span></span>
<span data-ttu-id="69250-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="69250-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69250-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="69250-129">-ResourceId</span></span>
<span data-ttu-id="69250-130">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="69250-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69250-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="69250-131">-Confirm</span></span>
<span data-ttu-id="69250-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69250-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69250-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69250-133">-WhatIf</span></span>
<span data-ttu-id="69250-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69250-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69250-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69250-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69250-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69250-136">CommonParameters</span></span>
<span data-ttu-id="69250-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69250-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69250-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69250-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69250-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69250-139">INPUTS</span></span>

### <span data-ttu-id="69250-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="69250-140">None</span></span>

## <span data-ttu-id="69250-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69250-141">OUTPUTS</span></span>

### <span data-ttu-id="69250-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="69250-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="69250-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69250-143">NOTES</span></span>

## <span data-ttu-id="69250-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69250-144">RELATED LINKS</span></span>
