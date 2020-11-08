---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268327"
---
# <span data-ttu-id="b9837-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b9837-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b9837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9837-102">SYNOPSIS</span></span>
<span data-ttu-id="b9837-103">Cihaz için yeni bir kullanıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9837-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="b9837-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9837-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9837-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9837-105">DESCRIPTION</span></span>
<span data-ttu-id="b9837-106">**New-AzDataBoxEdgeUser** cmdlet 'ı, veri kutusu Edge cihazı için yeni bir kullanıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9837-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="b9837-107">Yalnızca türü kullanıcıların oluşturulması `Share` desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b9837-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="b9837-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9837-108">EXAMPLES</span></span>

### <span data-ttu-id="b9837-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9837-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="b9837-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9837-110">PARAMETERS</span></span>

### <span data-ttu-id="b9837-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="b9837-111">-AsJob</span></span>
<span data-ttu-id="b9837-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b9837-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9837-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9837-113">-DefaultProfile</span></span>
<span data-ttu-id="b9837-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9837-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9837-115">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="b9837-115">-DeviceName</span></span>
<span data-ttu-id="b9837-116">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="b9837-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9837-117">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="b9837-117">-EncryptionKey</span></span>
<span data-ttu-id="b9837-118">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="b9837-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="b9837-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9837-119">-Name</span></span>
<span data-ttu-id="b9837-120">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="b9837-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9837-121">-Parola</span><span class="sxs-lookup"><span data-stu-id="b9837-121">-Password</span></span>
<span data-ttu-id="b9837-122">Parola, güvenli dize olarak sağla</span><span class="sxs-lookup"><span data-stu-id="b9837-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="b9837-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9837-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9837-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b9837-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9837-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="b9837-125">-Type</span></span>
<span data-ttu-id="b9837-126">UserType 'ı seçin</span><span class="sxs-lookup"><span data-stu-id="b9837-126">Select UserType</span></span>

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

### <span data-ttu-id="b9837-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b9837-127">-Confirm</span></span>
<span data-ttu-id="b9837-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b9837-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9837-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9837-129">-WhatIf</span></span>
<span data-ttu-id="b9837-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9837-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9837-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b9837-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9837-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9837-132">CommonParameters</span></span>
<span data-ttu-id="b9837-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9837-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9837-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b9837-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9837-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9837-135">INPUTS</span></span>

### <span data-ttu-id="b9837-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b9837-136">None</span></span>

## <span data-ttu-id="b9837-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9837-137">OUTPUTS</span></span>

### <span data-ttu-id="b9837-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b9837-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b9837-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9837-139">NOTES</span></span>

## <span data-ttu-id="b9837-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9837-140">RELATED LINKS</span></span>
