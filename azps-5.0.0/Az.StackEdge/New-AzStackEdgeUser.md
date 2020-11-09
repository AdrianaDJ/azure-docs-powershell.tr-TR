---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324994"
---
# <span data-ttu-id="03e02-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="03e02-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="03e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e02-102">SYNOPSIS</span></span>
<span data-ttu-id="03e02-103">Cihaz için yeni bir kullanıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03e02-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="03e02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03e02-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03e02-105">DESCRIPTION</span></span>
<span data-ttu-id="03e02-106">**New-AzStackEdgeUser** cmdlet 'ı yığın uç aygıtı için yeni bir kullanıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03e02-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="03e02-107">Yalnızca türü kullanıcıların oluşturulması `Share` desteklenir.</span><span class="sxs-lookup"><span data-stu-id="03e02-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="03e02-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03e02-108">EXAMPLES</span></span>

### <span data-ttu-id="03e02-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="03e02-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="03e02-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03e02-110">PARAMETERS</span></span>

### <span data-ttu-id="03e02-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="03e02-111">-AsJob</span></span>
<span data-ttu-id="03e02-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="03e02-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e02-113">-DefaultProfile</span></span>
<span data-ttu-id="03e02-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03e02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03e02-115">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="03e02-115">-DeviceName</span></span>
<span data-ttu-id="03e02-116">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="03e02-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e02-117">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="03e02-117">-EncryptionKey</span></span>
<span data-ttu-id="03e02-118">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="03e02-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="03e02-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="03e02-119">-Name</span></span>
<span data-ttu-id="03e02-120">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="03e02-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e02-121">-Parola</span><span class="sxs-lookup"><span data-stu-id="03e02-121">-Password</span></span>
<span data-ttu-id="03e02-122">Parola, güvenli dize olarak sağla</span><span class="sxs-lookup"><span data-stu-id="03e02-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="03e02-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e02-123">-ResourceGroupName</span></span>
<span data-ttu-id="03e02-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="03e02-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e02-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="03e02-125">-Type</span></span>
<span data-ttu-id="03e02-126">UserType 'ı seçin</span><span class="sxs-lookup"><span data-stu-id="03e02-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e02-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="03e02-127">-Confirm</span></span>
<span data-ttu-id="03e02-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03e02-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e02-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e02-129">-WhatIf</span></span>
<span data-ttu-id="03e02-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03e02-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03e02-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03e02-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e02-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e02-132">CommonParameters</span></span>
<span data-ttu-id="03e02-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03e02-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e02-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="03e02-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e02-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03e02-135">INPUTS</span></span>

### <span data-ttu-id="03e02-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="03e02-136">None</span></span>

## <span data-ttu-id="03e02-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03e02-137">OUTPUTS</span></span>

### <span data-ttu-id="03e02-138">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="03e02-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="03e02-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03e02-139">NOTES</span></span>

## <span data-ttu-id="03e02-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03e02-140">RELATED LINKS</span></span>
