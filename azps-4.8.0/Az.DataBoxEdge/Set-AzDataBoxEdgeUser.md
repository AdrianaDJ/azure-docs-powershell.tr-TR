---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275052"
---
# <span data-ttu-id="63d83-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="63d83-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="63d83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d83-102">SYNOPSIS</span></span>
<span data-ttu-id="63d83-103">Cihazda bir kullanıcı için yeni bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="63d83-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="63d83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63d83-104">SYNTAX</span></span>

### <span data-ttu-id="63d83-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63d83-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63d83-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="63d83-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63d83-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63d83-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63d83-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63d83-108">DESCRIPTION</span></span>
<span data-ttu-id="63d83-109">**Set-AzDataBoxEdgeUser** cmdlet 'ı, veri kutusu Edge cihazında bir kullanıcı için yeni bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="63d83-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="63d83-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63d83-110">EXAMPLES</span></span>

### <span data-ttu-id="63d83-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63d83-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="63d83-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63d83-112">PARAMETERS</span></span>

### <span data-ttu-id="63d83-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="63d83-113">-AsJob</span></span>
<span data-ttu-id="63d83-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="63d83-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63d83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d83-115">-DefaultProfile</span></span>
<span data-ttu-id="63d83-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63d83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63d83-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="63d83-117">-DeviceName</span></span>
<span data-ttu-id="63d83-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="63d83-118">Device Name</span></span>

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

### <span data-ttu-id="63d83-119">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="63d83-119">-EncryptionKey</span></span>
<span data-ttu-id="63d83-120">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="63d83-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="63d83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63d83-121">-InputObject</span></span>
<span data-ttu-id="63d83-122">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="63d83-122">Input Object</span></span>

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

### <span data-ttu-id="63d83-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="63d83-123">-Name</span></span>
<span data-ttu-id="63d83-124">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="63d83-124">Username</span></span>

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

### <span data-ttu-id="63d83-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="63d83-125">-Password</span></span>
<span data-ttu-id="63d83-126">Parola, güvenli dize olarak sağla</span><span class="sxs-lookup"><span data-stu-id="63d83-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="63d83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d83-127">-ResourceGroupName</span></span>
<span data-ttu-id="63d83-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="63d83-128">Resource Group Name</span></span>

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

### <span data-ttu-id="63d83-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63d83-129">-ResourceId</span></span>
<span data-ttu-id="63d83-130">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63d83-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="63d83-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="63d83-131">-Confirm</span></span>
<span data-ttu-id="63d83-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63d83-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63d83-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d83-133">-WhatIf</span></span>
<span data-ttu-id="63d83-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63d83-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63d83-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63d83-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63d83-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d83-136">CommonParameters</span></span>
<span data-ttu-id="63d83-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63d83-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d83-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63d83-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d83-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63d83-139">INPUTS</span></span>

### <span data-ttu-id="63d83-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="63d83-140">None</span></span>

## <span data-ttu-id="63d83-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63d83-141">OUTPUTS</span></span>

### <span data-ttu-id="63d83-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="63d83-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="63d83-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63d83-143">NOTES</span></span>

## <span data-ttu-id="63d83-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63d83-144">RELATED LINKS</span></span>
